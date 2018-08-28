# Image

> 图片

-------------

## 引入

```javascript
import { Image } from 'bh-mint-ui2';

Vue.component(Image.name, Image);
```

## 例子

`src` 属性为图片的地址。

`width` 属性为图片的宽度。

`height` 属性为图片的高度。

`top` 属性为图片距离顶部的距离。

`left` 属性为图片距离左边的距离。




<div>定宽定高</div>

```html
<mt-image
src="http://res.wisedu.com/fe_components/images/errorTip/no_search_result2.png"
width="200px" height="200px"></mt-image>
```


<div>图片100%自适应</div>


```html
<mt-image
src="http://res.wisedu.com/fe_components/images/errorTip/System_upgrade.png" @click="handleClick">
</mt-image>
```



## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| src | 图片的地址 | String | | '' |
| width | 图片的宽度 | String | | '' |
| height | 图片的高度 | String | | '' |
| top | 图片的顶部位置 | String | | '' |
| left | 图片的左侧位置 | String | | '' |



## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 点击 | `原生dom事件` |
