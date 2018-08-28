# Popup

> 弹出框，可自定义内容。

-------------

## 引入

```javascript
import { Popup } from 'bh-mint-ui2';

Vue.component(Popup.name, Popup);
```

## 例子

`position` 属性指定了 `popup` 的位置。比如，`position` 为 'bottom' 时，`popup` 会从屏幕下方移入，并最终固定在屏幕下方。移入/移出的动效会根据 `position` 的不同而自动改变，无需手动配置。

将 `v-model` 绑定到一个本地变量，通过操作这个变量即可控制 `popup` 的显示与隐藏。

```html
<mt-popup
  v-model="popupVisible"
  position="bottom">
  ...
</mt-popup>
```

若省略 `position` 属性，则 `popup` 会相对于屏幕居中显示（若不想让其居中，可通过 CSS 对其重新定位）。此时建议将动效设置为 `popup-fade`，这样在显示/隐藏时会有淡入/淡出效果。

```html
<mt-popup
  v-model="popupVisible"
  popup-transition="popup-fade">
  ...
</mt-popup>
```


底部弹窗对话框的代码示例

```html
<mt-popup v-model="popupVisible4" position="bottom">
  <div style="height:244px;background-color:#e8e8e8;">
    <div style="padding:12px 20px;background-color:#fff;font-size:17px">
      <span style="float:left;">申请陈述：</span>
      <span style="float:right;color:#06c1ae" @click="popupVisible4 = false">提交</span>
      <div style="clear: both;display:table;margin-bottom:5px"></div>
    </div>
    <mt-cell-group style="margin-bottom:4px">
      <mt-textarea maxlength=100 rows=4 placeholder="请输入"></mt-textarea>
    </mt-cell-group>
    <mt-button size="large">取消</mt-button>
  </div>
</mt-popup>
```

```js
export default {
  data() {
    return {
      popupVisible4: false
    }
  }
}
```

## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| position | `popup` 的位置。省略则居中显示 | String | 'top'<br>'right'<br>'bottom'<br>'left' | |
| pop-transition | 显示/隐藏时的动效，仅在省略 `position` 时可配置 | String | 'popup-fade' | |
| modal | 是否创建一个 modal 层 | Boolean | | true |
| closeOnClickModal | 是否可以通过点击 modal 层来关闭 `popup` | Boolean | | true |

## Slot
| name | 描述 |
|------|--------|
| - | 弹出框的内容 |
