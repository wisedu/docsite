# 如何扩展 EmapForm 组件的自定义类型( xtype)

下面使用一个自定义富文本编辑器类型（my-editor）介绍如何合理的对 emapform 的 xtype 进行扩展。

> 示例代码基于 vue 框架，其他框架同样可以参考

### vue 组件封装

首先将想要实现的自定义模块封装到一个 vue 组件，详见注释

```html
/// file: myEditor.vue
<template>
    <div>
        <input type="text" v-model='title'><!--标题-->
        <emap-editor v-ref:editor></emap-editor><!--内容-->
    </div>
</template>
<script>
    /**
     * 自定义针对 my-editor 类型的校验规则
     * 校验规则只需要初始化一次，最好直接放在组件头部定义
     */
    const MAX_LEN = 500
    WIS_EMAP_INPUT.allValidateRules['my-editor'] = {
        alertText: `不超过${MAX_LEN}字`, // 校验不通过自动提示的信息
        func (val) { // 函数名称必须为 func
            let content = val.content
            return content && content.length <= MAX_LEN // 校验内容是否超出长度
        }
    }
    // vue 组件定义
    export default {
        data: () => ({
            title: '' // 输入标题
        }),
        methods: { // 定义 setter 和 getter，名称随意
            getValue () {
                let content = this.$refs.editor.getValue()
                return {content, title: this.title} // 返回的是一个对象，校验时注意格式
            },
            setValue (val) { // 设置 value，注意同样的格式
                this.title = val.title
                this.$refs.editor.setValue(val.content)
            }
        },
        xtype: 'my-editor'
        // ... 其他设置略
    }
</script>
```

### 自定义类型挂载

定义完组件后要在 EmapForm 的类型库中注册才能被正确解析，注册过程建议单独放在一个文件中，方便维护。（下面的实现提供了一个较为通用的方案，所以略繁琐）

```javascript
/// file: myEditorControl.js
import MyEditor from './myEditor'

let registerd = {} // 防止定义重复的 xtype 名称

function register(vm, xtypeName) { // 可以在此处将组件默认名称替换为自定义
    let typeName = MyEditor.xtype || xtypeName
    if (registerd[typeName]) { // 此类型已经注册过了
        return
    }

    let compName = 'newxtype-' + typeName // 再加一层保护，使名称尽量唯一
    let refName = compName.replace(/-(\w)/g, (a, b) => b.toLowerCase()) // ref名字必须为小写
    Vue.component(compName, MyEditor)

    WIS_EMAP_INPUT.extend({ // 此处的参数必须按下面的方式定义
        xtype: typeName,
        init: function (ele, params) {
            ele.html(`<${compName} v-ref:${refName}></${compName}>`)
            vm.$nextTick(() => {
                vm.$compile(ele[0])
            })
        },
        setValue: function (ele, name, val, root) {
            return vm.$refs[refName].setValue(val)
        },
        getValue: function (ele, formData) {
            return vm.$refs[refName].getValue()
        },
        //... 提供其他 enable、disable 之类的接口，大体一样
    })

    registerd[typeName] = true
}

export default {register}

```

### 开箱即用

基于上面的两个文件，即可为业务页面提供一种通用的开箱即用方式：

meta 文件中使用新的类型，注意必须同时指定 xtype 和 checkType 才会生效：
```yaml
#...
form: {
  editor: {
    "name": "article",
    "dataType": "string",
    "caption": "文章",
    "xtype": "my-editor",
    "required": true,
    "checkType": "my-editor",
    "placeholder": "不超过500字"
  }
}
#...
```

页面不需做特殊的处理，只要将用到的自定义类型注册下：
```html
<template>
    <emap-form :options='...'></emap-form> <!-- 正常定义 -->
</template>
<script>
    require('./myEditorControl').register() // 注册此类型
    // 其他东东不变
</script>
```

### 完善

基于上述的实现，最佳的方式是维护一个公共的控件库，然后积累自定义的业务控件类型，提供统一的类型定义（防止冲突）与注册入口，方便复用与维护。
