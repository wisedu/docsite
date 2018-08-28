# Field

> 表单编辑器。

----------

## 引入

```javascript
import { Field } from 'bh-mint-ui2';

Vue.component(Field.name, Field);
```

## 例子

基础用法

```html
<mt-cell-group>
  <mt-field label="用户名" placeholder="请输入用户名" v-model="username" required></mt-field>
  <mt-field label="邮箱" placeholder="请输入邮箱" type="email" v-model="email"></mt-field>
  <mt-field label="密码" placeholder="请输入密码" type="password" v-model="password"></mt-field>
  <mt-field label="手机号" placeholder="请输入手机号" type="tel" v-model="phone"></mt-field>
  <mt-field label="网站" placeholder="请输入网址" type="url" v-model="website"></mt-field>
  <mt-field label="数字" placeholder="请输入数字" type="number" v-model="number"></mt-field>
  <mt-field label="生日" placeholder="请输入生日" type="date" v-model="birthday"></mt-field>
  <mt-field label="自我介绍" placeholder="自我介绍" type="textarea" rows="4" v-model="introduction" required :heightAuto="false"></mt-field>
  <mt-field label="自我介绍" placeholder="自我介绍" type="textarea" rows="4" required direction="vertical"></mt-field>
</mt-cell-group>
```


设置校验状态

```html
<mt-cell-group>
  <mt-field label="邮箱" state="success" v-model="email"></mt-field>
  <mt-field label="邮箱" state="error" v-model="email"></mt-field>
  <mt-field label="邮箱" state="warning" v-model="email"></mt-field>
</mt-cell-group>
```


自定义内容（例如添加验证码）

```html
<mt-cell-group>
  <mt-field label="验证码" v-model="captcha">
    <img src="../assets/100x100.png" height="45px" width="100px">
  </mt-field>
</mt-cell-group>
```


## API

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| type | 输入框类型 | String | text, number, email, url, tel, date, datetime, password, textarea | text |
| label| 标签 | String | | |
| value| 绑定表单输入值 | String | | |
| rows | 类型为 textarea 时可指定高度（显示行数），当`heightAuto=true`功能失效 | Number | | |
| placeholder | 占位内容 |String | | |
| disableClear | 禁用 clear 按钮 | Booean | | false |
| readonly | readonly |Boolean | | false |
| disabled | disabled |Boolean | | false |
| state | 校验状态 | String | error, success, warning | |
| attr | 设置原生属性，例如 `:attr="{ maxlength: 10 }"` | Object | |
| heightAuto | 该属性当且仅当`type="textarea"`时有效，设置文本输入框（textarea）高度自适应。此时rows属性无效 | Boolean | | true |
| required | 标注是否为必选项(*) | Boolean | | false |
| direction | 该属性当且仅当`type="textarea"`时有效，用于设置textarea上下结构布局,默认水平结构 | String | `vertical` | - |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| change  | 输入变化时触发 |  `变更后的值`,`原始dom事件`  |
| input  | 输入时触发，可以使用v-model双向绑定 |  `输入的值`  |

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
