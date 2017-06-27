# emapForm 模型

## 基本使用方法

```js
var formModel = [{
    "name": "DWDM",
    "caption": "问题B",
    "optionData":[
        {"id": "0", "name": "选项A"},
        {"id": "1", "name": "选项B"},
        {"id": "2", "name": "选项C"}
    ],
    "xtype": "checkboxlist",
    "dataSize": 6
}];
$('#horizonEditForm').emapForm({
  data: formModel,
  ...
});
```

## 模型的可选项全集包括如下：

| 属性 | 描述 | 数据类型 | 默认值 |
| :--- | :--- | :--- | :--- |
| name | 数据项名称 | String | 空 |
| caption | 显示文字 | String | 空 |
| xtype | 显示控件类型 | Enum | text |
| hidden | 是否隐藏 | Boolean | false |
| placeholder | 提示文字 | String | 空 |
| optionData | 数据选项 | Array | 空 |
| required | 必填 | Boolean | false |
| defaultValue | 默认值 | String | 空 |
| format | 日期、数字组件专用 | String | 空 |
| col | 所占列数 | Integer | 1 |
| dataSize | 最大长度校验值 | Integer | 空 |
| checkType | 校验类型 | Enum | 空 |
| JSONParam | 传递个实际组件的参数 | Object | 空 |

#### xtype

种类与效果，见上方的在线示例

#### checkType

| 名称 | 描述 |
| :--- | :--- |
| required | 必填校验 |
| double | 小数 |
| tele/tel | 电话号码 |
| phone | 手机号 |
| email/mail | 邮箱 |
| integer | 整数 |
| integer+0 | 非负整数 |
| integer+ | 正整数 |
| money | 金额数 |
| score | 分数 |
| number | 数字 |
| date | 日期 YYYY-MM-DD |
| ipv4 | ip地址 |
| url | url地址 |
| onlyNumberSp | 只能填写数字 |
| onlyLetterSp | 只能填写英文字母 |
| onlyLetterNumber | 只能填写数字与英文字母 |
| chinese | 只能填写中文汉字 |
| chinaId | 身份证号 |
| chinaIdLoose | 身份证号宽松匹配 |
| chinaZip | 中国邮编 |
| qq | qq |
| maxLength | 长度校验 |
| before | 日期早于联动字段，联动校验配置示例 before@CSRQ，其中CSRQ为联动字段的name |
| before= | 日期早于等于联动字段，联动校验配置示例 before=@CSRQ，其中CSRQ为联动字段的name |
| after | 日期晚于联动字段，联动校验配置示例 after@CSRQ，其中CSRQ为联动字段的name |
| after= | 日期晚于等于联动字段，联动校验配置示例 after=@CSRQ，其中CSRQ为联动字段的name |

#### JSONParam

该参数中的值将会被传递给实例化组件，用于个性化参数设置，例如{'displayMember':'name'}
![](/assets/ddtable1.png)

### col

字段所占列数，只在只读表单和表格表单中生效，可选值 1 2 3

```js
var formModel = [{
    ...
    col:3
    ...
}];
```



