# emapm-form
>移动端emap表单
***
## 支持的功能

>根据emap模型渲染表单组件，支持只读模式，提供校验、联动、分组、取值、赋值、显示、隐藏、disable、enable、必填、不必填和组件替换等功能

***
目前支持的显示类型

组件内部xtype | 名称
---- | ----
emtextarea | 文本域
emnumber | 数字
emselect | 下拉(带搜索功能)
emmulti-select | 多选下拉(有复选框)(带搜索功能)
emmulti-select2 | 多选下拉(旧)(带搜索功能)
emswitcher | 开关
emdate-local | 日期
emdate-full | 日期及时间
emradiolist | 单选组
emuploadsingleimage | 单图片上传
emuploadmuiltimage | 多图片上传
emselecttable | 下拉表格
emuploadfile | 上传文件（只读）
embuttonlist | 按钮组
emmulti-buttonlist | 多选按钮组

## 引入
#### 引入http://res.wisedu.com/fe_components/mobile/emap-mobile.min.js
## 例子
```javascript
<template>
    <emapm-form :model="model" v-model="formValue" :custom-vm="customVm" ref="form" :readonly="readonly"></emapm-form>
</template>
<script>
    export default {
    data() {
        return {
            model: model.controls,
            formValue: {
                WID: "test1"
            },
            customVm: {
                // '_text': customVm
            },
            readonly: false
        }
    }
}
</script>
```

## API
#### 表单

 名称 | 类型 | 是否必填 | 默认值 | 说明 
 ---- | ---- | ---- | ---- | ---- 
 model | Array | 是 | [] | emap模型 
 formValue | Object | 是 | {} | 表单的值 
 readonly | Boolean | 否 | false | 表单是否只读 
 customVm | Object | 否 | {} | 自定义的组件，用于替换表单里默认的显示类型组件 
>customVm
新增或替换模型xtpe对应的处理组件，详见下方<添加或替换组件>

#### 模型JSON控制参数

 模型类型 | 名称 | 参数类型 | 默认值 | 说明 
 ---- | ---- | ---- | ---- | ---- 
 下拉 | search | Boolean | true | 是否开启搜索功能 
 多选下拉(有复选框) | search | Boolean | true | 是否开启搜索功能 
 多选下拉(旧) | search | Boolean | true | 是否开启搜索功能 
 日期 | min | String | void | 日期范围最小值，例：1990-01-01
 日期 | max | String | void | 日期范围最大值，例：2999-01-01
 日期及时间 | min | String | void | 日期范围最小值，例：1990-01-01 00:00
 日期及时间 | max | String | void | 日期范围最大值，例：2999-01-01 00:00
 多图片上传 | limit | Number | 9 | 上传图片数 
 文本域/上传文件 | showTitle | Boolean | false | 是否展示标题


## Methods
 名称 | 参数 | 返回值 | 说明 
 ---- | ---- | ---- | ----
 validate | void | Boolean | 校验，支持的校验和PC端保持一致 
 getVmByName | String | vm | 获取模型字段对应组件实例，方便调用原子组件方法 
 showItem | String/Array | void | 参数为字段name或者name组成的数组，显示字段 
 hideItem | String/Array | void | 参数为字段name或者name组成的数组，隐藏字段 
 enableItem | String/Array | void | 参数为字段name或者name组成的数组，启用字段 
 disableItem | String/Array | void | 参数为字段name或者name组成的数组，禁用字段 
 requireItem | String/Array | void | 参数为字段name或者name组成的数组，改为必填字段 
 unRequireItem | String/Array | void | 参数为字段name或者name组成的数组，改为非必填字段

## 添加或替换组件

1、customVm
例：
```javascript
<template>
    <base-select :label="model.caption" :options="options" v-model="currentValue" :select-type="selectType" :placeholder="param.placeholder" :display-value="displayValue" :required="param.required" @display-change="handleDisplayChange" :readonly="param.readonly" :disabled="param.disabled" :search="param.search" ref="select"></base-select>
</template>
<script>
import baseSelect from '../baseComponents/baseSelect/baseSelect.vue';
export default {

    name: 'emSelect',

    props: {
        model: {
            type: Object,
            default: function() {
                return {};
            }
        },
        value: { default: '' },
        displayValue: { default: '' },
        options: {
            type: Array,
            default: function() {
                return [];
            }
        }
    },

    data() {
        return {
            currentValue: this.value
        };
    },

    computed: {
        param() {
            return this.model.initParam;
        },
        selectType() {
            if (this.model.xtype === 'select') {
                return 'select';
            }
            if (this.model.xtype === 'multi-select' || this.model.xtype === 'multi-select2') {
                return 'multi-select';
            }
        }
    },

    watch: {
        value(val) {
            this.currentValue = val;
        },
        currentValue(val) {
            this.$emit('input', val);
        }
    },

    methods: {
        handleDisplayChange(val) {
            this.$emit('update:displayValue', val);
        }
    },

    components: {
        baseSelect
    }
}
</script>
```

2、slot
>替换或新增模型字段处理组件，slot属性为模型项name，如果定义slot-scope="scope"，可通过scope取到model、value、displayValue，参数含义见下方自定义组件编写规范

例：
```javascript
<emapm-form :model="model" v-model="formValue" :custom-vm="customVm" ref="form" :readonly="readonly">
    <div slot="XM" slot-scope="scope">{{scope.model.caption}}</div>
</emapm-form>
```

### 自定义组件编写规范
可接收参数
```javascript
{
    model: {                        //模型
        type: Object,
        default: function() {
            return {};
        }
    },
    value: { default: '' },         //字段的值
    displayValue: { default: '' }   //字段展示值
}
```
>model内部有扩展出的initParam字段，方便控制组件展示，该字段的项为hidden、readonly、placeholder、disabled和JSONParam的字段，内部处理方法如下
```javascript
let jsonParam = parseParam(meta.JSONParam);
meta.initParam = Object.assign({
    hidden: meta.hasOwnProperty('form.hidden') ? meta['form.hidden'] : meta.hidden,
    readonly: readonly || (meta.hasOwnProperty('form.readonly') ? meta['form.readonly'] : meta.readonly),
    placeholder: meta.hasOwnProperty('form.placeholder') ? meta['form.placeholder'] : meta.placeholder,
    required: meta.hasOwnProperty('form.required') ? meta['form.required'] : meta.required,
    disabled: false
}, jsonParam);
```

可触发事件
>sync-change，同步数据到formValue，第一个参数是值，第二个参数为key
>input，同步字段值到formValue，参数是值
>update:displayValue，同步展示值到formValue，参数是值

注意：当组件的值改变后，需要将值同步到formValue，否则表单取值和校验会不准确
