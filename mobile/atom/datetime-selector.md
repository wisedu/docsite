# Datetime Selector

> 日期时间选择器，支持自定义类型。可在表单中使用

-------------

## 引入

```javascript
import { DatetimeSelector } from 'bh-mint-ui2';

Vue.component(DatetimeSelector.name, DatetimeSelector);
```

## 例子

`v-model` 属性为组件的绑定值，如："2018-12-31 12:00"。

`type` 属性表示 `datetime-selector` 组件的类型，它有三个可能的值：
*  `datetime`: 日期时间选择器，可选择年、月、日、时、分，`value` 值为一个 `Date` 对象
*  `date`: 日期选择器，可选择年、月、日，`value` 值为一个 `Date` 对象
*  `time`: 时间选择器，可选择时、分，`value` 值为一个格式为 `HH:mm` 的字符串

```html
<mt-datetime-selector label="日期时间" placeholder="请输入发生时间" type="datetime" value="2018-08-02 11:12" disableClear :maxHour="20" required></mt-datetime-selector>
<mt-datetime-selector label="日期(年月)" placeholder="请选择年月" type="dateym"  v-model="current1" :min-date="new Date(new Date().getFullYear() - 20, 0)" :max-date="new Date(new Date().getFullYear() + 20, 11)"></mt-datetime-selector>
<mt-datetime-selector label="日期时间(年月日)" placeholder="限制日期选择区间" type="date" v-model="current2" :min-date="new Date(new Date().getFullYear() - 20, 0,1)" :max-date="new Date(new Date().getFullYear() + 20, 11,31)"></mt-datetime-selector>
<mt-datetime-selector label="时间" placeholder="限制时间选择区间" type="time" :min-hour="10" :max-hour="15" ></mt-datetime-selector>
```

field 控制参数

```html
<mt-datetime-selector label="日期" placeholder="只读" type="date" :readonly="true">
</mt-datetime-selector>
<mt-datetime-selector label="日期" placeholder="禁用" type="date" :disabled="true">
</mt-datetime-selector>
<mt-datetime-selector label="日期" placeholder="没有清除按钮" type="date" :disable-clear="true">
</mt-datetime-selector>
<mt-datetime-selector label="日期" placeholder="成功" type="date" state="success">
</mt-datetime-selector>
<mt-datetime-selector label="日期" placeholder="错误" type="date" state="error">
</mt-datetime-selector>
<mt-datetime-selector label="日期" placeholder="警告" type="date" state="warning">
</mt-datetime-selector>
```


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| type | 组件的类型 | String | 'datetime', 'dateym', 'date', 'time' | 'datetime' |
| label | 标题 | String | | '' |
| placeholder | 占位文字 | String | | '' |
| value | 绑定表单输入值 | String | | |
| minDate | 可选的最小日期 | `Date` | 十年前的 1 月 1 日 | - |
| maxDate | 可选的最大日期 | `Date` | 十年后的 12 月 31 日 | - |
| minHour | 可选的最小小时 | `Number` | `0` | - |
| maxHour | 可选的最大小时 | `Number` | `23` | - |
| visibileColumnCount | 每一列可见备选元素的个数 | `Number` | `5` | - |
| placeholder | 占位内容 |String | | |
| disableClear | 禁用 clear 按钮 | Booean | | false |
| readonly | readonly |Boolean | | false |
| disabled | disabled |Boolean | | false |
| state | 校验状态 | String | error, success, warning | |
| attr | 设置原生属性，例如 `:attr="{ maxlength: 10 }"` | Object | |

## Events
| 事件名称 | 说明 | 回调参数 |
|------|-------|---------|
| confirm | 点击确认按钮时的回调函数 | `目前的选择值` |
| cancel | 点击取消按钮时的回调函数 |  |
| input | 选中值变化时触发，可以使用v-model双向绑定 | `变化后的值` |

