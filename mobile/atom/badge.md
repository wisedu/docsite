# Badge

> 徽章，可指定颜色和尺寸。

-----------

## 引入

```javascript
import { Badge } from 'bh-mint-ui2';

Vue.component(Badge.name, Badge);
```

## 例子

指定尺寸

```html
<mt-badge size="small">8</mt-badge>
<mt-badge size="normal">8</mt-badge>
<mt-badge size="large">8</mt-badge>
```

指定类型

```html
<mt-badge type="primary">8</mt-badge>
<mt-badge type="danger">10</mt-badge>
<mt-badge type="success">30</mt-badge>
<mt-badge type="warning">100</mt-badge>
```

自定义

```html
<mt-badge type="danger" size="small">10</mt-badge>
<mt-badge padding="3px" color="red"></mt-badge>
<mt-badge size="normal" padding="3px" color="#FFB950" radius="2px">卷</mt-badge>
<mt-badge padding="4px" color="#FFF" fontColor="#FFB950" bColor="#FFB950" radius="2px">自动缴费</mt-badge>
```

## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| type | 显示类型 | String | primary, danger, success, warning | primary|
| color | 自定义背景颜色值| String | | type 的颜色 |
| size | 尺寸 | String | normal, large, small | normal |
| fontColor | 字体色 | String |  |  |
| fontSize | 字体大小 | String |  |  |
| padding | 内边距 | String |  |  |
| radius | 边框倒角 | String |  |  |
| bColor | 边框色 | String |  |  |
## Slot
| name | 描述 |
|------|--------|
| - | 显示内容 |
