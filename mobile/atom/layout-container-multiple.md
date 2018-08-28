# LayoutContainerMultiple(LayoutContainerMultipleItem)

> 多列容器（或栅格容器）

------------

## 引入

```javascript
import { LayoutContainerMultiple } from 'bh-mint-ui2';

Vue.component(LayoutContainerMultiple.name, LayoutContainerMultiple);
```

## 例子


```html
<mt-layout-container-multiple>
    <mt-layout-container-multiple-item width="33.33%">左侧容器</mt-layout-container-multiple-item>
    <mt-layout-container-multiple-item width="33.33%">中间容器</mt-layout-container-multiple-item>
    <mt-layout-container-multiple-item width="33.33%">右侧容器</mt-layout-container-multiple-item>
</mt-layout-container-multiple>
```


## API(LayoutContainerMultipleItem)
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| width | 尺寸 | String |  |  |

## Events(LayoutContainerMultipleItem)
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 点击时触发 | `原始dom事件`  |


