# Hr

> 分割线

-------------

## 引入

```javascript
import { Hr } from 'bh-mint-ui2';

Vue.component(Hr.name, Hr);
```

## 例子

`height` 属性为分割线的高度，线的粗细。

`margin` 属性为分割线的外边距。

`background` 属性为分割线的背景颜色。


默认
```html
<mt-hr></mt-hr>
```

粗的线,带外边距
```html
<mt-hr height="4px" margin="10px 0"></mt-hr>
```

颜色primary
```html
<mt-hr background="#52C7CA"></mt-hr>
```

颜色warning
```html
<mt-hr background="#FFB950"></mt-hr>
```

颜色danger
```html
<mt-hr background="#F26666"></mt-hr>
```



## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| height | 分割线的高度 | String | | '0.5px' |
| margin | 分割线的外边距 | String | | '' |
| background | 分割线的背景颜色 | String | | '#E8E8E8' |


