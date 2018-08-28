<style>
.mint-navbar.is-fixed{
    position: relative !important;
}
.mint-navbar .mint-tab-item.is-selected{
    margin-bottom: 0 !important;
}

.mint-fixed-button{
    position: absolute !important;
}
div[smile-category="FixedButton"] > .smile-classify-item-content{
    min-height: 110px;
}
</style>

# FixedButton

> 浮动按钮，永久浮动在页面上。

------------

## 引入

```javascript
import { FixedButton } from 'bh-mint-ui2';

Vue.component(FixedButton.name, FixedButton);
```

## 例子
浮动位置

```html
<mt-fixed-button position="bottom-right">+</mt-fixed-button>
<mt-fixed-button position="bottom-left">+</mt-fixed-button>
<mt-fixed-button position="top-right">+</mt-fixed-button>
<mt-fixed-button position="top-left">+</mt-fixed-button>
```

样式类型

```html
<mt-fixed-button type="primary">+</mt-fixed-button>
<mt-fixed-button type="warning">+</mt-fixed-button>
<mt-fixed-button type="danger">+</mt-fixed-button>
<mt-fixed-button type="grey">+</mt-fixed-button>
```

内容大小

```html
<mt-fixed-button size="20px">+</mt-fixed-button>
```

内容颜色

```html
<mt-fixed-button color="green">+</mt-fixed-button>
```

圆角
```html
<mt-fixed-button borderRadius="100%">+</mt-fixed-button>
```

背景
```html
<mt-fixed-button background="red">+</mt-fixed-button>
```

宽高
```html
<mt-fixed-button width="40px" height="40px">+</mt-fixed-button>
```

浮动位置微调
```html
<mt-fixed-button left="40px" top="40px">+</mt-fixed-button>
<mt-fixed-button right="40px" buttom="40px">+</mt-fixed-button>
```

内容距离按钮顶部位置微调
```html
<mt-fixed-button contentmargintop="10px">+</mt-fixed-button>
```

绑定 click 事件
```html
<mt-fixed-button @click.native="handleClick">+</mt-fixed-button>
```

## API

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| position | 浮动(fixed)位置 | String | bottom-right, <br>bottom-left, <br>top-right, <br>top-left | bottom-right(bottom:20px;right:16px) |
| type | 显示样式 | String |  primary,<br> danger,<br> warning,<br> grey,<br>red,orange,yellow,green,blue,indigo,purple,white等 | primary |
| size | 尺寸 | String |  | 18px |
| borderRadius | 圆角 | String | | 50% |
| color | 内容颜色 | String | | '' |
| background | 背景 | String | | '' |
| width | 宽度 | String | | 46px |
| height | 高度 | String | | 46px |
| left | 距离左侧位置 | String | | 16px |
| right | 距离右侧位置 | String | | 16px |
| top | 距离顶部位置 | String | | 20px |
| buttom | 距离底部位置 | String | | 20px |
| contentmargintop | 内容距离按钮顶部位置 | String | | '' |


## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 按钮点击时触发 | `原始dom事件`  |
