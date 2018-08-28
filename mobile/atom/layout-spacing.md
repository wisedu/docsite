# LayoutSpacing

> 空白间距行。

------------

## 引入

```javascript
import { LayoutSpacing } from 'bh-mint-ui2';

Vue.component(LayoutSpacing.name, LayoutSpacing);
```

## 例子
默认

```html
<mt-layout-spacing></mt-layout-spacing>
```


背景

```html
<mt-layout-spacing background="rgba(0,0,0,0.1)"></mt-layout-spacing>
```

高度

```html
<mt-layout-spacing height="30px" background="grey"></mt-layout-spacing>
```

边框

```html
<mt-layout-spacing border="0.5px solid #52C7CA" :borderside="borderside"></mt-layout-spacing>
```

## API

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| background | 背景 | String |  |  |
| height | 高度 | String |  |"15px"|
| border | 边框 | String |  |  |
| borderside | 边框项（配合border使用） | Array |  |  |

