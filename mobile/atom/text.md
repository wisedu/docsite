# Text

> 文本

-------------

## 引入

```javascript
import { Text } from 'bh-mint-ui2';

Vue.component(Text.name, Text);
```

## 例子


默认

```html
<mt-text>默认文本</mt-text>
```



字体大小

```html
<mt-text size="20px">20px</mt-text>
```



可换肤颜色

```html
<mt-text type="grey">grey文本</mt-text>
<mt-text type="primary">primary文本</mt-text>
<mt-text type="warning">warning文本</mt-text>
<mt-text type="danger">danger文本</mt-text>
<mt-text type="white">white文本</mt-text>
<mt-text type="red">red文本</mt-text>
<mt-text type="orange">orange文本</mt-text>
<mt-text type="yellow">yellow文本</mt-text>
<mt-text type="green">green文本</mt-text>
<mt-text type="blue">blue文本</mt-text>
<mt-text type="indigo">indigo文本</mt-text>
<mt-text type="purple">purple文本</mt-text>
```



自定义颜色

```html
<mt-text color="#F334AB">grey文本</mt-text>
```



自定义字体

```html
<mt-text size="20px">20px</mt-text>
```



## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| type | 可换肤颜色 | String | `grey` `primary` `warning` `danger` `white` `red` `orange` `yellow` `green` `blue` `indigo` `purple`| `grey` |
| color | 自定义颜色 | String |  |  |
| size | 尺寸 | String |  |  |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 点击时触发 | `原始dom事件`  |
