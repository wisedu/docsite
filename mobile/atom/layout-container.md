# LayoutContainer

> 普通容器，相当于div

------------

## 引入

```javascript
import { LayoutContainer } from 'bh-mint-ui2';

Vue.component(LayoutContainer.name, LayoutContainer);
```

## 例子

背景

```html
<mt-layout-container background="gray">普通容器</mt-layout-container>
```

外边距(与css的margin用法相同)

```html
<mt-layout-container margin="10px" background="gray">普通容器</mt-layout-container>
```

内边距(与css的padding用法相同)

```html
<mt-layout-container padding="10px" background="gray">普通容器</mt-layout-container>
```


绑定 click 事件

```html
<mt-layout-container @click.native="handleClick">普通容器</mt-layout-container>
```


## API

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| background | 背景 | String | | |
| margin | 外边距 | String | | |
| padding | 内边距 | String | | |


