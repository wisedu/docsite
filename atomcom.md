# 原子组件

### 如何获取

通过以下两种方式都可以使用原子组件

##### 在页面引用

```html
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont_2.0/iconfont.css">
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh.min.css">
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes.min.css">
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bh_utils.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/jqwidget/jqxwidget.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bhtc/moment/min/moment-with-locales.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bh.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/emap.js"></script>
```

##### 使用ubase集成

index.html

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="renderer" content="webkit">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/prism/prism.css">
    <!-- commomlib include jquery.js jquery.nicescroll.js jquery.fileupload.js director.min.js hogan.min.js lodash.min.js globalize.js-->
    <script src="http://res.wisedu.com/fe_components/commonlib.js"></script>
    <!-- 此处可以放置第三方库-->
    <script src="http://res.wisedu.com/fe_components/prism/prism.js"></script>
    <script src="http://res.wisedu.com/fe_components/appcore.js"></script>
</head>
<body>
</body>
</html>
```

## 调用组件

大部分通用组件我们引用了jQwidget，其官方帮助文档：[http://www.jqwidgets.com/jquery-widgets-demo/](http://www.jqwidgets.com/jquery-widgets-demo/)

考虑性能，我们对包尺寸有所缩减，我们仅包括了使用频率较高

1. jqxButtons

2. jqxCalendar

3. jqxInput

4. jqxComboBox

5. jqxDateTimeInput

6. jqxDataAdapter

7. jqxDropDownList

8. jqxListBox

9. jqxLoader

10. jqxMenu

11. jqxNotification

12. jqxNumberInput

13. jqxPanel

14. jqxPopOver

15. jqxScrollBar

16. jqxTabs

17. jqxTextArea

18. jqxTooltip

19. jqxTree

20. jqxValidator

21. jqxWindow

22. jqxProgressBar

23. jqxNavigationBar

24. jqxDragDrop

更多组件我们采用了三方插件 和 我们的特色组件（bh组件）

请参考本章节下面的每个组件示例

