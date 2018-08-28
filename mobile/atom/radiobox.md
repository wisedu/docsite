# Radiobox

> 复选框列表，依赖 <router-link to="cell">cell</a> 组件。

-------------

## 引入

```javascript
import { Radiobox } from 'bh-mint-ui2';

Vue.component(Radiobox.name, Radiobox);
```

## 例子

#### 基础用法
通过`v-model`绑定 radiobox 的勾选状态，`提示：点击已经选中项的文字标题，可以取消选择`


```html
<mt-radiobox v-model="value1">复选框 1</mt-radiobox>
<mt-radiobox v-model="value2" disabled>禁用的复选框</mt-radiobox>
```

```javascript
export default {
  data() {
    return {
      value1: false,
      value2: true
    };
  }
};
```


#### box-group

需要与`mt-box-group`一起使用，在`mt-radio-group`通过`v-model`来绑定当前选中的值。

```html
<mt-box-group v-model="value3">
    <mt-cell-group>
        <mt-radiobox :name="item.value" :disabled="item.disabled" v-for="item in options" :key="item.value">
            {{item.label}}
        </mt-radiobox>
        <mt-cell title="选中的项">{{ value3 }}</mt-cell>
    </mt-cell-group>
</mt-box-group>
```


选择框右对齐

```html
<mt-box-group v-model="value4" align="right">
    <mt-cell-group>
        <mt-radiobox align="right" :name="item.value" :disabled="item.disabled" v-for="item in options" :key="item.value">
            {{item.label}}
        </mt-radiobox>
        <mt-cell title="选中的项">{{ value4 }}</mt-cell>
    </mt-cell-group>
</mt-box-group>
```



选中还可以组合其他内容在里面哦

```html
<mt-box-group v-model="value5">
    <mt-cell-group>
        <mt-radiobox ref="cb" :name="item" v-for="item in options1" :key="item">
            {{item}}
            <div slot="newline" slot-scope="scope" style="margin-top:10px" v-if="scope.checked">
                <mt-textarea maxlength="50" placeholder="请输入你的答案"></mt-textarea>
            </div>
        </mt-radiobox>
    </mt-cell-group>
</mt-box-group>
```

横向布局（注：选项不多于三个）
```html
<mt-cell-group title="横向单选">
  <mt-radiobox direction="horizon" name="性别" v-model="value" wrapperpaddingleft="0" :options="options"></mt-radiobox>
  <mt-cell title="选中的项">{{ value }}</mt-cell>
</mt-cell-group>
```
```javascript
export default {
  data() {
    return {
      value: "",
    }
  },
  created() {
    this.options = [
      {
        id:"1",
        label:"男"
      },
      {
        id:"2",
        label:"女"
      },
      {
        id:"3",
        label:"禁用",
        disabled: true
      }
    ]
  }
};
```

## Radiobox API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
|name | 标识 Radiobox 名称 | string | | |
|disabled | 是否禁用单选框 | Boolean | | false |
|align| 复选框对其位置| String | left, right | left |
|direction| 显示布局方式 | String | `vertical`, `horizon` | `vertical` |
|options| 横向布局参数 | Array | - | [] |
|required | 标注是否为必选项(*),仅在`direction='horizon'`有效 | Boolean | | false |
|wrapperpaddingleft | 自定义cell左侧内边距,仅在`direction='horizon'`有效 | String | | '' |

## radiobox Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| input  | 输入值变化时触发，可以使用v-model双向绑定 | `变化后的值`  |


### BoxGroup API

| 参数 | 说明 | 类型 | 默认值 | 可选值 |
|-----------|-----------|-----------|-------------|-------------|
| disabled | 是否禁用所有单选框 | `Boolean` | `false` | - |


### BoxGroup Event

| 事件名称 | 说明 | 回调参数 |
|-----------|-----------|-----------|
| change | 当绑定值变化时触发的事件 | 当前组件的值 |

<script>
  export default {
    data: function(){
      return {
        value1:false,
        value2:true,
        value3:"选中禁用的值",
        value4:"",
        value5:"选项A",
        options:[
          {
            label: '被禁用',
            value: '值F',
            disabled: true
          },
          {
            label: '选中禁用',
            value: '选中禁用的值',
            disabled: true
          },
          {
            label: '选项A',
            value: '值A'
          },
          {
            label: '选项B',
            value: '值B'
          }
        ],
        options1:['选项A', '选项B', '选项C']
      }
    },
    methods:{
    }
  };
</script>
