# Action sheet

> 操作表，从屏幕下方移入。

-------------

## 引入

```javascript
import { Actionsheet } from 'bh-mint-ui2';

Vue.component(Actionsheet.name, Actionsheet);
```

## 例子

`actions` 属性绑定一个由对象组成的数组，每个对象有 `name` 和 `method` 两个键，`name` 为菜单项的文本，`method` 为点击该菜单项的回调函数。

将 `v-model` 绑定到一个本地变量，通过操作这个变量即可控制 `actionsheet` 的显示与隐藏。

```html
<mt-actionsheet
  :actions="actions"
  v-model="sheetVisible">
</mt-actionsheet>
```

## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| actions | 菜单项数组 | Array | | |
| cancelText | 取消按钮的文本。若设为空字符串，则不显示取消按钮 | String | | '取消' |
| closeOnClickModal | 是否可以通过点击 modal 层来关闭 `actionsheet` | Boolean | | true |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| input  | 选中值变化时触发，可以使用v-model双向绑定 | `变化后的值`  |
| click  | 点击项后触发 | `项`,`顺序值`,`原始dom事件`  |
