# Button

> 按钮，提供几种基础样式和尺寸，可自定义图标。

------------

## 引入

```javascript
import { Button } from 'bh-mint-ui2';

Vue.component(Button.name, Button);
```

## 例子
改变颜色

```html
<mt-button type="default">default</mt-button>
<mt-button type="primary">primary</mt-button>
<mt-button type="danger">danger</mt-button>
```

改变大小

```html
<mt-button size="small">small</mt-button>
<mt-button size="large">large</mt-button>
<mt-button size="normal">normal</mt-button>
```

禁用按钮

```html
<mt-button disabled>disabled</mt-button>
```

幽灵按钮

```html
<mt-button plain>plain</mt-button>
```

带图标

```html
<mt-button icon="back">back</mt-button>
<mt-button icon="more">更多</mt-button>
```

自定义图标

```html
<mt-button>
  <img src="" height="20" width="20" slot="icon">
  带自定义图标
</mt-button>
```

绑定 click 事件

```html
<mt-button @click="handleClick">点击触发 handleClick</mt-button>
```

## API

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| plain | 幽灵按钮 | Boolean | | false |
| disabled | 禁用状态 | Boolean | | false |
| type | 按钮显示样式 | String |  default, primary, danger | default |
| size | 尺寸 | String | small, normal, large | normal |
| icon | 图标 | String | more, back | |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 按钮点击时触发 | `原始dom事件`  |

## Slot
| name | 描述 |
|------|--------|
| - | 显示的文本内容|
| icon | 自定义显示的图标|

