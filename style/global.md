# 全局样式

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<style>
.bh-border{
	width:120px;
	height: 55px;
	font-size: 12px;
	margin: 5px;
}
.bh-border.bh-color-primary-4, .bh-border.bh-color-primary-5,
.bh-border.bh-color-info-4, .bh-border.bh-color-info-5,
.bh-border.bh-color-success-4, .bh-border.bh-color-success-5,
.bh-border.bh-color-warning-4, .bh-border.bh-color-warning-5,
.bh-border.bh-color-danger-4, .bh-border.bh-color-danger-5,
.bh-border.bh-color-grey-4, .bh-border.bh-color-grey-5{
	background-color: rgba(0,0,0,0.25);
}
.boxmargin{
	float:left;
	border:8px solid #f4b865;
}
.boxborder{
	width:120px;
	height: 75px;
	border:1px solid #333;
}
.boxpadding{
	border:8px solid #93d36e;
	width: 100%;
    height: 100%;
}
.box-border-mp-h{
	border-top: none;
	border-bottom: none;
}
.box-border-mp-v{
	border-left: none;
	border-right: none;
}
.box-border-mp-t{
	border-left: none;
	border-right: none;
	border-bottom: none;
}
.box-border-mp-b{
	border-top: none;
	border-left: none;
	border-right: none;
}
</style>

## 文字

<h1>H1 这是标题1 </h1>
<h2>H2 这是标题2 </h2>
<h3>H3 这是标题3 </h3>
<h4>H4 这是标题4 </h4>
<h5>H5 这是标题5 </h5>
<h6>H6 这是标题6 </h6>
<p><span class="bh-text-caption bh-color-caption">这是标准说明文字 </span></p>
<p><span class="bh-text-caption-large bh-color-caption">这是大号的默认说明文字</span></p>
```html
<h1>H1 这是标题1 </h1> 
<h2>H2 这是标题2 </h2> 
<h3>H3 这是标题3 </h3> 
<h4>H4 这是标题4 </h4> 
<h1>H5 这是标题5 </h5> 
<h6>H6 这是标题6 </h6> 
<span class="bh-text-caption bh-color-caption">这是默认说明文字</span>
<span class="bh-text-caption-large bh-color-caption">这是大号的默认说明文字</span>
```


## 边距

bh-m和bh-p定义margin和padding，预定义4 8 16 24 32五种距离
* mh = margin horizontal，表示左右外边距
* mv = margin vertical，表示上下外边距
* mt = margin top，表示底部外边距
* mb = margin bottom，表示底部外边距
* ph = padding horizontal，表示左右内边距
* pv = padding vertical，表示上下内边距
* pt = padding top，表示顶部内边距
* pb = padding bottom，表示底部内边距。


<div class="boxmargin bh-m-8">
	<div class="boxborder">
		<div class="boxpadding"></div>
	</div>
</div>

```html
<div class="bh-m-8 bh-p-8"></div>
```

<div class="boxmargin bh-m-16 box-border-mp-h">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-h"></div>
	</div>
</div>

<div class="boxmargin bh-m-8 box-border-mp-v">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-v"></div>
	</div>
</div>

<div class="boxmargin bh-m-8 box-border-mp-t">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-t"></div>
	</div>
</div>

<div class="boxmargin bh-m-16 box-border-mp-b">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-b"></div>
	</div>
</div>


<div class="bh-clearfix"></div>



| 距离 | 4px | 8px | 16px | 24px | 32px | 
| :--- | :--- | :--- | :--- | :--- | :--- |
| 外边距 | .bh-m-4 | .bh-m-8 | .bh-m-16 | .bh-m-24 | .bh-m-32 | 
| 左右外边距 | .bh-mh-4 | .bh-mh-8 | .bh-mh-16 | .bh-mh-24 | .bh-mh-32 | 
| 上下外边距 | .bh-mv-4 | .bh-mv-8 | .bh-mv-16 | .bh-mv-24 | .bh-mv-32 | 
| 顶部外边距 | .bh-mt-4 | .bh-mt-8 | .bh-mt-16 | .bh-mt-24 | .bh-mt-32 | 
| 底部外边距 | .bh-mb-4 | .bh-mb-8 | .bh-mb-16 | .bh-mb-24 | .bh-mb-32 | 
| 内边距 | .bh-p-4 | .bh-p-8 | .bh-p-16 | .bh-p-24 | .bh-p-32 | 
| 左右内边距 | .bh-ph-4 | .bh-ph-8 | .bh-ph-16 | .bh-ph-24 | .bh-ph-32 | 
| 上下内边距 | .bh-pv-4 | .bh-pv-8 | .bh-pv-16 | .bh-pv-24 | .bh-pv-32 | 
| 顶部内边距 | .bh-pt-4 | .bh-pt-8 | .bh-pt-16 | .bh-pt-24 | .bh-pt-32 | 
| 顶部内边距 | .bh-pb-4 | .bh-pb-8 | .bh-pb-16 | .bh-pb-24 | .bh-pb-32 | 


## 颜色
### 字体色

<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-color-primary">bh-color-primary</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-primary-2">bh-color-primary-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-primary-3">bh-color-primary-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-primary-4">bh-color-primary-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-primary-5">bh-color-primary-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-color-info">bh-color-info</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-info-2">bh-color-info-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-info-3">bh-color-info-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-info-4">bh-color-info-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-info-5">bh-color-info-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-color-success">bh-color-success</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-success-2">bh-color-success-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-success-3">bh-color-success-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-success-4">bh-color-success-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-success-5">bh-color-success-5</div>
</div>

<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-color-warning">bh-color-warning</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-warning-2">bh-color-warning-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-warning-3">bh-color-warning-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-warning-4">bh-color-warning-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-warning-5">bh-color-warning-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-color-danger">bh-color-danger</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-danger-2">bh-color-danger-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-danger-3">bh-color-danger-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-danger-4">bh-color-danger-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-danger-5">bh-color-danger-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-color-grey">bh-color-grey</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-grey-2">bh-color-grey-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-grey-3">bh-color-grey-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-grey-4">bh-color-grey-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-color-grey-5">bh-color-grey-5</div>
</div>

使用示例，在class中使用
```html
<div class="bh-color-primary">bh-color-primary</div>
<div class="bh-color-primary-2">bh-color-primary-2</div>
<div class="bh-color-primary-3">bh-color-primary-3</div>
<div class="bh-color-primary-4">bh-color-primary-4</div>
<div class="bh-color-primary-5">bh-color-primary-5</div>
```




### 背景色

<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-primary bh-color-primary-5">bh-bg-primary</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-primary-2">bh-bg-primary-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-primary-3">bh-bg-primary-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-primary-4">bh-bg-primary-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-primary-5">bh-bg-primary-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-info bh-color-info-5">bh-bg-info</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-info-2">bh-bg-info-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-info-3">bh-bg-info-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-info-4">bh-bg-info-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-info-5">bh-bg-info-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-success bh-color-success-5">bh-bg-success</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-success-2">bh-bg-success-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-success-3">bh-bg-success-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-success-4">bh-bg-success-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-success-5">bh-bg-success-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-warning bh-color-warning-5">bh-bg-warning</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-warning-2">bh-bg-warning-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-warning-3">bh-bg-warning-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-warning-4">bh-bg-warning-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-warning-5">bh-bg-warning-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-danger bh-color-danger-5">bh-bg-danger</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-danger-2">bh-bg-danger-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-danger-3">bh-bg-danger-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-danger-4">bh-bg-danger-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-danger-5">bh-bg-danger-5</div>
</div>
<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-grey bh-color-grey-5">bh-bg-grey</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-grey-2">bh-bg-grey-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-grey-3">bh-bg-grey-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-grey-4">bh-bg-grey-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bg-grey-5">bh-bg-grey-5</div>
</div>

使用示例，在class中使用
```html
<div class="bh-bg-primary bh-color-primary-5">bh-bg-primary</div>
<div class="bh-bg-primary-2">bh-bg-primary-2</div>
<div class="bh-bg-primary-3">bh-bg-primary-3</div>
<div class="bh-bg-primary-4">bh-bg-primary-4</div>
<div class="bh-bg-primary-5">bh-bg-primary-5</div>
```



### 边框色

<div class="bh-clearfix bh-mb-4">
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-primary">bh-bColor-primary</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-primary-2">bh-bColor-primary-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-primary-3">bh-bColor-primary-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-primary-4">bh-bColor-primary-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-primary-5">bh-bColor-primary-5</div>
</div>

<div class="bh-clearfix bh-mb-4">
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-info">bh-bColor-info</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-info-2">bh-bColor-info-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-info-3">bh-bColor-info-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-info-4">bh-bColor-info-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-info-5">bh-bColor-info-5</div>
</div>

<div class="bh-clearfix bh-mb-4">
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-success">bh-bColor-success</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-success-2">bh-bColor-success-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-success-3">bh-bColor-success-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-success-4">bh-bColor-success-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-success-5">bh-bColor-success-5</div>
</div>

<div class="bh-clearfix bh-mb-4">
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-warning">bh-bColor-warning</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-warning-2">bh-bColor-warning-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-warning-3">bh-bColor-warning-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-warning-4">bh-bColor-warning-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-warning-5">bh-bColor-warning-5</div>
</div>

<div class="bh-clearfix bh-mb-4">
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-danger">bh-bColor-danger</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-danger-2">bh-bColor-danger-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-danger-3">bh-bColor-danger-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-danger-4">bh-bColor-danger-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-danger-5">bh-bColor-danger-5</div>
</div>

<div class="bh-clearfix">
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-grey">bh-bColor-grey</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-grey-2">bh-bColor-grey-2</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-grey-3">bh-bColor-grey-3</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-grey-4">bh-bColor-grey-4</div>
    <div class="bh-pull-left bh-border bh-p-8 bh-bColor-grey-5">bh-bColor-grey-5</div>
</div>

使用示例，在class中使用
```html
<div class="bh-bColor-primary">bh-bColor-primary</div>
<div class="bh-bColor-primary-2">bh-bColor-primary-2</div>
<div class="bh-bColor-primary-3">bh-bColor-primary-3</div>
<div class="bh-bColor-primary-4">bh-bColor-primary-4</div>
<div class="bh-bColor-primary-5">bh-bColor-primary-5</div>
```

