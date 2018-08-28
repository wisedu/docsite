# Icon

> 字体图标

----------


## 引入

```javascript
import { icon } from 'bh-mint-ui2';

Vue.component(icon.name, icon);
```

## 例子

基础用法

```html
<mt-icon name="icon-pinglun"></mt-icon>
<mt-icon name="icon-pinglun" size="30px"></mt-icon>
```



`name` 是字体图标库的图标class。图标地址是：http://res.wisedu.com/fe_components/iconfont_mobile/demo_fontclass.html

设置图标内边距

```html
<mt-icon name="icon-pinglun" padding="20px"></mt-icon>
```

设置图标颜色

```html
<mt-icon name="icon-pinglun" color="red"></mt-icon>
```


设置字体图标点击之后的颜色

```html
<mt-icon name="icon-pinglun" changecolor="red"></mt-icon>
```

`changecolor` 是字体图标点击之后的颜色。

设置图标点击事件

```html
<mt-icon name="icon-pinglun" @click="doSome"></mt-icon>
```

```javascript
methods:{
  doSome () {
    alert('you are clcik');
  }
}
```

设置字体图标点击时的动画

```html
<mt-icon name="icon-pinglun" animate="animated shake"></mt-icon>
```

`animate` 是给字体图标设置点击动画样式。动画由Animate.css提供：https://daneden.github.io/animate.css/?


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| name  |  图标样式   | String    |    |     |
| size | 图标大小 | String | | |
| padding  | 图标内边距 | String | | |
| color | 图标颜色 | String | | |
| changecolor | 图标点击之后的颜色 | String | | |
| animate | 图标点击时的动画效果 | String | | |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 按钮点击时触发 | `原始dom事件`  |
