# Select

> 选择器

-----------

## 引入

```javascript
import { Select } from 'bh-mint-ui2';

Vue.component(Select.name, Select);
```

## 例子

单选select

```html
<mt-select label="单选" :options="singleSelectOptions" v-model="singleSelectValue" select-type="select" @selector-click="singleSelectClick">
</mt-select>
<p>{{singleSelectValue}}</p>
```


多选select

```html
<mt-select label="多选" :options="multiSelectOptions" v-model="multiSelectValue" select-type="multi-select" @selector-click="multiSelectClick">
</mt-select>
<p>{{multiSelectValue}}</p>
```


自定义

```html
<mt-select label="自定义选择" :options="yearSlot" v-model="value" select-type="custom">
  <template slot-scope="scope" slot="display">{{scope.value}}</template>
  <template slot-scope="scope" slot="selector">
    <mt-cell v-for="item in scope.options" :key="item" :class="{active: item === scope.value}" :title="item" @click.native.stop="selectClick(item)" wrapperpaddingleft="20px"></mt-cell>
  </template>
</mt-select>
<p>{{value}}</p>
```



## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| label | 字段中文名 | String | - | - |
| value | 字段绑定值 | String | - | - |
| placeholder | 占位文字 | String | - | "请选择" |
| options | 选项数据 | Array | - | [] |
| select-type | select形式 | String | `select`,`multi-select`,`custom` | `select` |
| titlewidth | 自定义title标签所占宽度 | String | | '' |
| valueAlign | 设定value内容的对齐方式 | String | `flex-start`,`flex-end`,'center' |  |
| readonly | 只读模式 | Boolean | | false |
| disabled | 无效模式 | Boolean | | false |
| required | 标注是否为必选项(*) | Boolean | | false |

<script>
  export default {
    methods: {
      singleSelectClick: function () {
        this.singleSelectOptions = this.dicSlot
      },
      multiSelectClick: function () {
        this.multiSelectOptions = this.dicSlot
      },
      customSelectClick: function () {
        this.customSelectOptions = this.dicSlot
      },
      selectClick (item) {
        this.customSelectValue = item.id
        if (window.location.hash.indexOf('smile-select') > -1) {
          history.back()
        }
      },
      getDisplay (id, options) {
        const option = options.filter(item => item.id === id)[0]
        return option ? option.name : ''
      }
    },
    data: function() {
    return {
      singleSelectValue: '',
      singleSelectOptions: [],

      multiSelectValue: '',
      multiSelectOptions: [],

      customSelectValue: '',
      customSelectOptions: [],

      dicSlot: [
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
    }
  }
};
</script>

## Slot

| name | 描述 |
|------|--------|
| display | 自定义select 获取值显示 |
| selector | 自定义select 所有值的显示 |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| selector-click  | 点击选择器时触发 | `当前值`,`原始dom事件`  |
