# PC样式

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<style>
.book-summary{
	font-size:14px;
}
.box{
	width:120px;
	height: 55px;
	font-size: 16px;
	margin: 5px;
	color:white;
	text-align: center;
}
</style>




### 字体图标库

[字体图标库1](http://res.wisedu.com/fe_components/iconfont/demo.html)
```html
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">
```

[字体图标库2](http://res.wisedu.com/fe_components/iconfont_2.0/demo_fontclass.html)
```html
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont_2.0/iconfont.css">
```

### 如何获取

引用如下文件

```html
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont_2.0/iconfont.css">
```

由于该样式是基于jQWidget组件作为基础，进行定制修改的，所以文件存放在jqwidget子目录中

### 换肤

更换路径中主题包的文件夹名即可：

如，blue 主题：

* /fe_components/jqwidget/**`blue`**/bh-1.2.min.css
* /fe_components/jqwidget/**`blue`**/bh-scenes-1.2.min.css

purple 主题

* /fe_components/jqwidget/**`purple`**/bh-1.2.min.css
* /fe_components/jqwidget/**`purple`**/bh-scenes-1.2.min.css

#### 颜色主题列表

<div class="bh-clearfix">
	<div class="box bh-pull-left" style="background-color: #3E50B4">blue</div>
	<div class="box bh-pull-left" style="background-color: #734184">purple</div>
	<div class="box bh-pull-left" style="background-color: #5677FC">lightBlue</div>
	<div class="box bh-pull-left" style="background-color: #009688">green</div>
	<div class="box bh-pull-left" style="background-color: #990099">colorE</div>
	<div class="box bh-pull-left" style="background-color: #3F51B5">indigo<br>靛蓝</div>
	<div class="box bh-pull-left" style="background-color: #009587">teal<br>水鸭绿</div>
	<div class="box bh-pull-left" style="background-color: #3A7E59">millennium<br>千禧绿</div>
	<div class="box bh-pull-left" style="background-color: #D22E2E">cherry<br>樱桃红</div>
	<div class="box bh-pull-left" style="background-color: #7A1EA1">magenta<br>绛紫</div>
	<div class="box bh-pull-left" style="background-color: #BB8235">golden<br>土豪金</div>
</div>

<!-- cyan-arctic
green-olive
red-strawberry
yellow-fawn -->


主题颜色的完整定义请参考：

* [交互设计规范1.2](http://res.wisedu.com/ID/1.SPEC/PC/PC-SPEC-V1.1-16.05.12%40%E8%8D%86%E5%A4%A9%E9%AA%90/#g=1&p=____-type_color)
* [平台门户颜色定义](http://res.wisedu.com/ID/2.CampuSphere/%E5%B9%B3%E5%8F%B0%E9%97%A8%E6%88%B7/Finish/PC-%E9%97%A8%E6%88%B7%E7%9A%AE%E8%82%A4%E9%85%8D%E7%BD%AE-V2.2-17.03.15%40%E8%8D%86%E5%A4%A9%E9%AA%90/#g=1&p=indigo-dark_____-_)


可换肤的样式：[请点这里](http://res.wisedu.com/FS/docsite/style/global.html#颜色)


#### 皮肤定制工具

http://res.wisedu.com:9090/custom/


### 平台换肤接口

通过平台JSONP接口获取皮肤

/jsonp/getUserSkin.json

获取skinName
```
{
    "skinName": "millennium",
    "siteType": 1,
    "hasLogin": true,
    "contextPath": "",
    "themeColor": "dark"
}
```


示例：http://ampdx.wisedu.com/jsonp/getUserSkin.json?amp_jsonp_callback=jQuery21104590702586970088_1523517816000&_=1523517816001


### UBASE框架集成

/config.js
```js
define(function(require, exports, module) {
	var config = {
		/*
		 * bh前端组件版本
		 */
		"BH_VERSION": "1.2",
		/*
			资源服务器地址
		 */
		"RESOURCE_SERVER": SERVER_PATH,
		"THEME": "blue",
		...
	};
	return config;
});
```

