# Search

> 搜索框，可显示搜索结果列表。

----------

## 引入

```javascript
import { Search } from 'bh-mint-ui2';

Vue.component(Search.name, Search);
```

## 例子

基础用法

```html
<mt-search v-model="value"></mt-search>
```


设置显示文字

```html
<mt-search
  v-model="value"
  cancel-text="取消"
  placeholder="搜索">
</mt-search>
```


带搜索结果

```html
<mt-search v-model="value" :result.sync="result"></mt-search>
```


自定义搜索结果

```html
<mt-search v-model="value">
  <mt-cell
    v-for="item in result"
    :key="item.value"
    :title="item.title"
    :value="item.value"
    @onFocus="handleFocus"
    @onBlur="handleBlur"
    @search="search">
  </mt-cell>
</mt-search>
```

事件方法：
```javaScript
methods:{
  handleFocus(value){
    console.log("focus:%s",value)
  },
  handleBlur(value){
    console.log("blur:%s",value)
  },
  search(value){
    console.log("search:%s",value)
  }
}
```




## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| value | 搜索结果绑定值  | String | |   |
| cancel-text | 取消按钮文字 | String | | 取消 |
| placeholder | 搜索框占位内容  | String | | 搜索 |
| result | 搜索结果列表 | Array | | |
| autofocus | 自动聚焦 | Boolean | - | false |
| show | 始终显示搜索列表 | Boolean | - | false |
| margintop | 搜索结果列表绝对定位的Top值 | String | - | `43px` |

## Slot

| name | 描述 |
|------|--------|
| - | 自定义搜索结果列表|


<script>
  export default {
    data: function(){
      return {
        value:"",
        result:[{value:"ok",title:"ok"}]
      }
    },
    methods:{
    }
  };
</script>

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| canceled  | 取消搜索时触发 | `原始dom事件`  |
| search  | 点击enter键时触发 | `原始dom事件`  |
| onFocus  | 获取焦点时触发 | `原始dom事件`  |
| onBlur  | 失去焦点时触发 | `原始dom事件`  |
