# Text Select

> 本文输入，有可选项辅助输入。配合表单Field使用

-------------

## 引入

```javascript
import { TextSelect } from 'bh-mint-ui2';

Vue.component(TextSelect.name, TextSelect);
```

## 例子

`v-model` 属性为组件的绑定值。


```html
<mt-text-select label="抄送人员" placeholder="请输入" rows="5" maxlength="100" :options="singleSelectOptions" v-model="singleSelectValue" @selector-click="singleSelectClick"></mt-text-select>
```
设置禁用选项
```javascript
import axios from 'axios'
export default {
  methods: {
    singleSelectClick () {
      //可以在点击时，做数据的异步加载，该案例中，数据是默认加载
      this.singleSelectOptions = [
        { id: 1, name: '奔波儿灞' },
        { id: 2, name: '霸波尔奔' },
        { id: 3, name: '金角大王' },
        { id: 4, name: '银角大王' },
        { id: 5, name: '虎力大仙' },
        { id: 6, name: '鹿力大仙' },
        { id: 7, name: '羊力大仙' },
        { id: 8, name: '黄袍怪' },
        { id: 9, name: '白骨精' },
        { id: 10, name: '小钻风' }
      ]
      // axios.get('/mock/userdata.json').then(resp => {
      //   let respData = resp.data
      //   if (respData.code == '0') {
      //     this.singleSelectOptions = respData.datas.code.rows
      //   }
      // })
    }
  },
  data: function() {
    return {
      singleSelectValue: '',
      singleSelectOptions: []
    }
  }
};
```


field 控制参数

::: demo
```html
<mt-text-select label="抄送人员" placeholder="只读" rows="5" maxlength="100" :readonly="true" :options="singleSelectOptions"></mt-text-select>
<mt-text-select label="抄送人员" placeholder="禁用" rows="5" maxlength="100" :disabled="true" :options="singleSelectOptions"></mt-text-select>
```
:::


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| label | 标题 | String | | '' |
| placeholder | 占位文字 | String | | '' |
| value | 绑定表单输入值 | String | | |
| rows | 点击后的文本域行数 | Number | | 4 |
| maxlength | 最大填写的字数 | Number | |  |
| readonly | readonly |Boolean | | false |
| disabled | disabled |Boolean | | false |
| attr | 设置原生属性，例如 `:attr="{ maxlength: 10 }"` | Object | |

## Events
| 事件名称 | 说明 | 回调参数 |
|------|-------|---------|
| selector-click | 选择器点击 |  |


<script>
import axios from 'axios'
export default {
  methods: {
    singleSelectClick () {
      //可以在点击时，做数据的异步加载，该案例中，数据是默认加载
      this.singleSelectOptions = [
        { id: 1, name: '奔波儿灞' },
        { id: 2, name: '霸波尔奔' },
        { id: 3, name: '金角大王' },
        { id: 4, name: '银角大王' },
        { id: 5, name: '虎力大仙' },
        { id: 6, name: '鹿力大仙' },
        { id: 7, name: '羊力大仙' },
        { id: 8, name: '黄袍怪' },
        { id: 9, name: '白骨精' },
        { id: 10, name: '小钻风' }
      ]
      // axios.get('/mock/userdata.json').then(resp => {
      //   let respData = resp.data
      //   if (respData.code == '0') {
      //     this.singleSelectOptions = respData.datas.code.rows
      //   }
      // })
    }
  },
  data: function() {
    return {
      singleSelectValue: '',
      singleSelectOptions: []
    }
  }
};
</script>

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| selector-click  | 点击选择器时触发 | `原始dom事件`  |
