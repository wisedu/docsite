# Checkbox

> 复选框列表，依赖 <router-link to="cell">cell</a> 组件。

-------------

## 引入

```javascript
import { Checkbox } from 'bh-mint-ui2';

Vue.component(Checkbox.name, Checkbox);
```

## 例子

#### 基础用法
通过`v-model`绑定 checkbox 的勾选状态

```html
<mt-cell-group>
  <mt-checkbox v-model="value1">复选框 1</mt-checkbox>
  <mt-checkbox v-model="value2" disabled>禁用的复选框</mt-checkbox>
</mt-cell-group>
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

需要与`mt-box-group`一起使用，选中值是一个数组，通过`v-model`绑定在`mt-box-group`上，数组中的项即为选中的`Checkbox`的`name`属性设置的值

同时设置最大可选数2

```html
<mt-box-group v-model="value3" :max="2">
    <mt-cell-group>
        <mt-checkbox :name="item.value" :disabled="item.disabled" v-for="item in options" :key="item.value">
            {{item.label}}
        </mt-checkbox>
        <mt-cell title="选中的项">{{ value3 }}</mt-cell>
    </mt-cell-group>
</mt-box-group>
```


选择框右对齐

```html
<mt-box-group v-model="value4" align="right">
    <mt-cell-group>
        <mt-checkbox align="right" :name="item.value" :disabled="item.disabled" v-for="item in options" :key="item.value">
            {{item.label}}
        </mt-checkbox>
        <mt-cell title="选中的项">{{ value4 }}</mt-cell>
    </mt-cell-group>
</mt-box-group>
```


选中还可以组合其他内容在里面哦

```html
<mt-box-group v-model="value5">
    <mt-cell-group>
        <mt-checkbox ref="cb" :name="item" v-for="item in options1" :key="item">
            {{item}}
            <div slot="newline" slot-scope="scope" style="margin-top:10px" v-if="scope.checked">
                <mt-textarea maxlength="50" placeholder="请输入你的答案"></mt-textarea>
            </div>
        </mt-checkbox>
    </mt-cell-group>
</mt-box-group>
```


## Checkbox API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
|name | 标识 Checkbox 名称 | string | | |
|disabled | 是否禁用单选框 | Boolean | | false |
|align| 复选框对其位置| String | left, right | left |


## Checkbox Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| input  | 输入值变化时触发，可以使用v-model双向绑定 | `变化后的值`  |


### BoxGroup API

| 参数 | 说明 | 类型 | 默认值 | 可选值 |
|-----------|-----------|-----------|-------------|-------------|
| disabled | 是否禁用所有单选框 | `Boolean` | `false` | - |
| max | 最多允许选择的数量 | `Number` |  | - |


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
        value3:["选中禁用的值"],
        value4:[],
        value5:["选项A"],
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
