## Picker 选择器

### 使用指南
``` javascript
import { Picker } from 'bh-mint-ui2';

Vue.component(Picker.name, Picker);
```

### 代码演示


#### 基础用法

```html
<mt-picker :columns="columns"  @change="onChange"/>
```

```javascript
export default {
  data() {
    return {
      columns: ['杭州', '宁波', '温州', '嘉兴', '湖州']
    };
  },
  onChange(picker, values,column) {
    Toast(`当前值：${value}, 当前索引：${column}`);
  }
};
```

#### 禁用选项、展示顶部栏
选项可以为对象结构，通过设置 disabled 来禁用该选项

```html
<mt-picker :columns="columns" @cancel="onCancel" @confirm="onConfirm" :title="标题" showToolbar/>
```

```javascript
export default {
  data() {
    return {
      columns: [
        { text: '杭州', disabled: true },
        { text: '宁波' },
        { text: '温州' }
      ]
    };
  }
};
```

#### 两级非联动

```html
<mt-picker :columns="column" :title="两级非联动" showToolbar @confirm="onConfirm" @cancel="onCancel" />
```

```javascript
export default {
  data() {
    return {
      columns: [{
        values:[
          {text:'浙江',disabled:false,id:101,pid:-1}, 
          {text:'福建',disabled:false,id:201,pid:-1},
          {text:'江苏',disabled:false,id:301,pid:-1}],
        className:'className1',
        defaultIndex: 2
      },{
        values:[
          {text:'杭州',disabled:false,pid:101,id:10101}, 
          {text:'宁波',disabled:true,pid:101,id:10102},
          {text:'温州',disabled:false,pid:101,id:10103},
          {text:'嘉兴',disabled:false,pid:101,id:10104},
          {text:'湖州',disabled:false,pid:101,id:10105},
          {text:'福州',disabled:false,pid:201,id:20101}, 
          {text:'厦门',disabled:false,pid:201,id:20102},
          {text:'莆田',disabled:false,pid:201,id:20103},
          {text:'三明',disabled:false,pid:201,id:20104},
          {text:'泉州',disabled:false,pid:201,id:20105},
          {text:'南京',disabled:false,pid:301,id:30101}, 
          {text:'扬州',disabled:false,pid:301,id:30102},
          {text:'无锡',disabled:false,pid:301,id:30103},
          {text:'常州',disabled:false,pid:301,id:30104},
          {text:'苏州',disabled:false,pid:301,id:30105}],
        className:'className2',
        defaultIndex: 2
      }]
    }
  },
  methods: {
    onConfirm(value, index) {
      console.log(value,index);
      //返回值（value）格式：[{text:'江苏',disabled:true,id:301,pid:-1}],{text:'无锡',disabled:false,pid:301,id:30103}]
    },
    onCancel() {
      Toast('取消');
    }
  }
};
```

#### 三级联动

```html
<div class="page-picker-wrapper">
  <mt-picker :columns="column" :title="三级联动" showToolbar @confirm="onConfirm" @cancel="onCancel" :isInterrelated="true"/>
</div>
```

```javascript
column:[
  {
    values:[
      {text:'浙江',disabled:false,id:101,pid:-1}, 
      {text:'福建',disabled:false,id:201,pid:-1},
      {text:'江苏',disabled:false,id:301,pid:-1}],
    className:'className1',
    defaultIndex: 1
  },{
    values:[
      {text:'杭州',disabled:false,pid:101,id:10101}, 
      {text:'宁波',disabled:true,pid:101,id:10102},
      {text:'温州',disabled:false,pid:101,id:10103},
      {text:'嘉兴',disabled:false,pid:101,id:10104},
      {text:'湖州',disabled:false,pid:101,id:10105},
      {text:'福州',disabled:false,pid:201,id:20101}, 
      {text:'厦门',disabled:false,pid:201,id:20102},
      {text:'莆田',disabled:false,pid:201,id:20103},
      {text:'三明',disabled:false,pid:201,id:20104},
      {text:'泉州',disabled:false,pid:201,id:20105},
      {text:'南京',disabled:false,pid:301,id:30101}, 
      {text:'扬州',disabled:false,pid:301,id:30102},
      {text:'无锡',disabled:false,pid:301,id:30103},
      {text:'常州',disabled:false,pid:301,id:30104},
      {text:'苏州',disabled:false,pid:301,id:30105}],
    className:'className2',
    defaultIndex: 0
  },
  {
    values:[
      {text:'上城区',disabled:false,pid:10101,id:101011},
      {text:'下城区',disabled:false,pid:10101,id:101012},
      {text:'西湖区',disabled:false,pid:10101,id:101013},
      {text:'鼓楼区',disabled:false,pid:30101,id:301011},
      {text:'玄武区',disabled:false,pid:30101,id:301012},
      {text:'江宁区',disabled:false,pid:30101,id:301013},
      {text:'邗江区',disabled:false,pid:30102,id:301021},
      {text:'江都区',disabled:false,pid:30102,id:301022},
      {text:'开发区',disabled:false,pid:30102,id:301023},
      {text:'江阴市',disabled:false,pid:30103,id:301031},
      {text:'宜兴市',disabled:false,pid:30103,id:301032},
      {text:'锡山区',disabled:false,pid:30103,id:301033},
      {text:'惠山区',disabled:false,pid:30103,id:301034},
      {text:'钟楼区',disabled:false,pid:30104,id:301041},
      {text:'武进区',disabled:false,pid:30104,id:301042},
      {text:'溧阳区',disabled:false,pid:30104,id:301043},
      {text:'姑苏区',disabled:false,pid:30105,id:301051},
      {text:'相城区',disabled:false,pid:30105,id:301052},
      {text:'吴江区',disabled:false,pid:30105,id:301053},
      {text:'虎丘区',disabled:false,pid:30105,id:301054},
      {text:'吴中区',disabled:false,pid:30105,id:301055},
      {text:'常熟市',disabled:false,pid:30105,id:301056}
    ],
    className:'className3'
  }
]

```

### API

| 参数 | 说明 | 类型 | 默认值 | 可选值 |
|-----------|-----------|-----------|-------------|-------------|
| columns | 对象数组，配置每一列显示的数据 | `Array` | `[]` | - |
| showToolbar | 是否显示顶部栏 | `Boolean` | `false` | - |
| confirmText | 确定按钮文本 | `String` | `确定` | - |
| cancelText | 取消按钮文本 | `String` | 默认'x' | - |
| title | 顶部栏标题 | `String` | `''` | - |
| itemHeight | 选项高度 | `Number` | `44` | - |
| visibileColumnCount | 可见的选项个数 | `Number` | `5` | - |
| valueKey | 选项对象中，文字对应的 key | `String` | `text` | - |
| isInterrelated | 标识columns数据是否关联，该属性在’多列联动1’数据时使用，达到多级数据的联动效果 | `Boolean` | `false` | - |

### Columns 数据结构
当传入多列数据时，`columns`为一个对象数组，数组中的每一个对象配置每一列，每一列有以下`key`

| key | 说明 |
|-----------|-----------|
| values | 列中对应的备选值 |
| defaultIndex | 初始选中项的索引，默认为 0 |
| className | 为对应列添加额外的`class` |

### Picker 实例
在`change`事件中，可以获取到`picker`实例，通过实例方法可以灵活控制 Picker 内容；`isInterrelated=true`,暂不支持`change`事件

| 函数 | 说明 |
|-----------|-----------|
| getValues() | 获取所有列选中的值，返回一个数组 |
| setValues(values) | 设置所有列选中的值 |
| getIndexes() | 获取所有列选中值对应的索引，返回一个数组 |
| setIndexes(indexes) | 设置所有列选中值对应的索引 |
| getColumnValue(columnIndex) | 获取对应列选中的值 |
| setColumnValue(columnIndex, value) | 设置对应列选中的值 |
| getColumnIndex(columnIndex) | 获取对应列选中项的索引 |
| setColumnIndex(columnIndex, optionIndex) | 设置对应列选中项的索引 |
| getColumnValues(columnIndex) | 获取对应列中所有选项 |
| setColumnValues(columnIndex, values) | 设置对应列中所有选项 |
