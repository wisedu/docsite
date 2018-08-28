# Datetime picker

> 日期时间选择器，支持自定义类型。

-------------

## 引入

```javascript
import { DatetimePicker } from 'bh-mint-ui2';

Vue.component(DatetimePicker.name, DatetimePicker);
```

## 例子

`v-model` 属性为组件的绑定值，如：
*  Date格式：new Date(2018, 11, 31,12,00);
*  字符串格式："2018-12-31 12:00"（推荐使用）;

`type` 属性表示 `datetime-picker` 组件的类型，它有三个可能的值：
*  `datetime`: 日期时间选择器，可选择年、月、日、时、分，`value` 值为一个 `Date` 对象
*  `date`: 日期选择器，可选择年、月、日，`value` 值为一个 `Date` 对象
*  `time`: 时间选择器，可选择时、分，`value` 值为一个格式为 `HH:mm` 的字符串

`datetime-picker` 提供了两个供外部调用的方法：`open` 和 `close`，分别用于打开和关闭选择器。

```html
<template>
  <mt-datetime-picker
  v-model="currentDate" type="datetime"
  ref="picker"
  :minHour="minHour" :maxHour="maxHour"
  :minDate="minDate" :maxDate="maxDate"/>
</template>

<script>
  export default {
    data() {
      return {
        minHour: 10,
        maxHour: 20,
        minDate: new Date(2008,0,31),
        maxDate: new Date(2028, 10, 1),
        currentDate: "2018-12-31 12:00"
      };
    }
  };
</script>
```


选择日期

```html
<mt-datetime-picker
  v-model="currentDate"
  type="date"
  :minDate="minDate"
/>
```


选择时间

```html
<mt-datetime-picker
  v-model="currentDate"
  type="time"
  :minHour="minHour"
  :maxHour="maxHour"
/>
```


当点击确认按钮时会触发 `confirm` 事件，参数为当前 value 的值。

```html
<mt-datetime-picker
  v-model="currentDate"
  type="time"
  @confirm="handleConfirm"
  @cancel="handleCancel">
</mt-datetime-picker>
```


当点击弹出的picker外层的遮罩时触发`maskCallback`事件，参数为固定值`'mask'`

```html
<mt-datetime-picker
  v-model="currentDate"
  type="time"
  :maskFun="true"
  @maskCallback="handleCancel">
</mt-datetime-picker>
```
```javaScript
<script>
  export default {
    data() {
      return {
        minHour: 10,
        maxHour: 20,
        minDate: new Date(),
        maxDate: new Date(2019, 10, 1),
        currentDate: new Date(2018, 0, 1)
      };
    },
    methods: {
      handleConfirm(value,picker){
        //value为当前值，picker为实例
      },
      handleCancel(value){
        //当cancel事件时，value=undefined;当maskCallback事件时，value=“mask”
      }
    }
  };
</script>
```

## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| type | 组件的类型 | `String` | 'datetime', 'date', 'time' | 'datetime' |
| cancelText | 取消按钮文本 | `String` | | '取消' |
| confirmText | 确定按钮文本 | `String` | | '确定' |
| minDate | 可选的最小日期 | `Date` | 十年前的 1 月 1 日 | - |
| maxDate | 可选的最大日期 | `Date` | 十年后的 12 月 31 日 | - |
| minHour | 可选的最小小时 | `Number` | `0` | - |
| maxHour | 可选的最大小时 | `Number` | `23` | - |
| visibileColumnCount | 每一列可见备选元素的个数(即显示的行数) | `Number` | `5` | - |
| maskFun | 开启遮罩返回函数（与maskCallback事件同时使用，默认不开启） | `Boolean` |  | false |


## Events
| 事件名称 | 说明 | 回调参数 |
|------|-------|---------|
| confirm | 点击确认按钮时的回调函数 | `目前的选择值` |
| cancel | 点击取消按钮时的回调函数 |  |
| input | 选中值变化时触发，可以使用v-model双向绑定 | `变化后的值` |
| maskCallback | 点击遮罩时的回调函数,当且仅当maskFun=true有效 | `mask` |

