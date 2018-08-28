# Textarea

> 文本域，配合Field使用。

----------

## 引入

```javascript
import { Textarea } from 'bh-mint-ui2';

Vue.component(Textarea.name, Textarea);
```

## 例子

基础用法

```html
<mt-textarea label="有标题" placeholder="全宽度" rows=3 maxlength=100 ></mt-textarea>
<mt-textarea placeholder="全宽度" rows=3 maxlength=100 ></mt-textarea>
```


设置校验状态

```html
<mt-textarea label="success" placeholder="success" rows=3 maxlength=50 state="success"></mt-textarea>
<mt-textarea label="error" placeholder="error" rows=3 maxlength=20 state="error"></mt-textarea>
<mt-textarea label="warning" placeholder="warning" rows=3 maxlength=10 state="warning"></mt-textarea>
<mt-textarea placeholder="右侧自定义内容" rows=3 maxlength=50>自定义</mt-textarea>
<mt-textarea placeholder="同时出现" rows=3 maxlength=20 state="error">
  <mt-icon type="icon-wifi"></mt-icon>
</mt-textarea>
```




## API

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| label| 标签 | String | | |
| value| 绑定表单输入值 | String | | |
| rows | 类型为 textarea 时可指定高度（显示行数），当`heightAuto=true`功能失效 | Number | | |
| maxlength | 最大填写的字数 | Number | |  |
| placeholder | 占位内容 |String | | |
| disableClear | 禁用 clear 按钮 | Booean | | false |
| readonly | readonly |Boolean | | false |
| disabled | disabled |Boolean | | false |
| state | 校验状态 | String | error, success, warning | |
| attr | 设置原生属性，例如 `:attr="{ maxlength: 10 }"` | Object | |
| titlepaddingtop | 左边标题距顶边距 | String | `0px` | |
| titlepaddingright | 左边标题距右边距 | String | `0px` | |
| titlepaddingbottom | 左边标题距下边距 | String | `0px` | |
| titlepaddingleft | 左边标题距左边距 | String | `0px` | |
| areapaddingtop | 右边内容距顶边距 | String | `0px` | |
| areapaddingright | 右边内容距右边距 | String | `0px` | |
| areapaddingbottom | 右边内容距下边距 | String | `0px` | |
| areapaddingleft | 右边内容距左边距 | String | `0px` | |
| heightAuto | 该属性当且仅当`type="textarea"`时有效，设置文本输入框（textarea）高度自适应。此时rows属性无效 | Boolean | | true |
| required | 标注是否为必选项(*) | Boolean | | false |
| direction | 该属性当且仅当`type="textarea"`时有效，用于设置textarea上下结构布局,默认水平结构 | String | `vertical` | - |

## Slot
| name | 描述 |
|------|--------|
| - | 显示的 HTML 内容|

<script>
  export default {
    data: function(){
      return {
        username:"",
        email:"",
        password:"",
        phone:"",
        website:"",
        number:"",
        birthday:"",
        introduction:"",
        captcha:""
      }
    },
    methods:{
    }
  };
</script>

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| change  | 输入内容改变时触发 |  `原始dom事件`  |
