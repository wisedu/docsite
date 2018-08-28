# LayoutLeftRight(LayoutLeftRightItem)

> 左右双栏容器（flex布局）。

------------

## 引入

```javascript
import { LayoutLeftRight } from 'bh-mint-ui2';

Vue.component(LayoutLeftRight.name, LayoutLeftRight);
```

## 例子
flex默认等分

```html
<mt-layout-left-right>
  <mt-layout-left-right-item slot="left"><div class="mt-bg-primary mt-color-white">左flex:1</div></mt-layout-left-right-item>
  <mt-layout-left-right-item slot="right"><div class="mt-bg-warning mt-color-white">右flex:1</div></mt-layout-left-right-item>
</mt-layout-left-right>
```


flex布局百分比设置

```html
<mt-layout-left-right>
  <mt-layout-left-right-item slot="left"  percentage="30"><div class="mt-bg-primary mt-color-white">左30%</div></mt-layout-left-right-item>
  <mt-layout-left-right-item slot="right"  percentage="70"><div class="mt-bg-warning mt-color-white">右70%</div></mt-layout-left-right-item>
</mt-layout-left-right>
```

flex布局像素设置

```html
<mt-layout-left-right>
  <mt-layout-left-right-item slot="left"  percentage="100px"><div class="mt-bg-primary mt-color-white">左60px</div></mt-layout-left-right-item>
  <mt-layout-left-right-item slot="right"  percentage="calc(100% - 100px)"><div class="mt-bg-warning mt-color-white">右(100%-40px)</div></mt-layout-left-right-item>
</mt-layout-left-right>
```

flex左右布局子元素比例分配

```html
<mt-layout-left-right>
  <mt-layout-left-right-item slot="left"  percentage="2"><div class="mt-bg-primary mt-color-white">左60px</div></mt-layout-left-right-item>
  <mt-layout-left-right-item slot="right"  percentage="1"><div class="mt-bg-warning mt-color-white">右(100%-40px)</div></mt-layout-left-right-item>
</mt-layout-left-right>
```

绑定 click 事件
```html
<mt-layout-left-right @click.native="handleClick">点击触发 handleClick</mt-layout-left-right>
```

## API(LayoutLeftRightItem)
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| percentage | 容器宽度 | String |  |  |

## Slot
| name | 描述 |
|------|--------|
| left | 左侧容器|
| right | 右侧容器|

