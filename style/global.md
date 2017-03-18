# 全局样式

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<style>
.book-summary{
	font-size:14px;
}
.box{
	width:120px;
	height: 55px;
	font-size: 12px;
	margin: 5px;
}
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
<h5>H5 这是标题5 </h5> 
<h6>H6 这是标题6 </h6> 
<span class="bh-text-caption bh-color-caption">这是默认说明文字</span>
<span class="bh-text-caption-large bh-color-caption">这是大号的默认说明文字</span>
```


## 边距

bh-m和bh-p定义margin和padding，预定义4 8 16 24 32五种距离
<div class="boxmargin bh-mb-16 bh-mh-24">
	<div class="boxborder">
		<div class="boxpadding">内容</div>
	</div>
</div>

```html
<div class="bh-m-8 bh-p-8">内容</div>
m = margin，表示外边距
p = padding，表示内边距。
```

<div class="bh-clearfix"></div>


<div class="boxmargin box-border-mp-h bh-mb-16 bh-mh-24">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-h">内容</div>
	</div>
</div>

```html
<div class="bh-mh-8 bh-ph-8">内容</div>
mh = margin horizontal，表示左右外边距
ph = padding horizontal，表示左右内边距
```

<div class="bh-clearfix"></div>

<div class="boxmargin bh-mb-16 box-border-mp-v bh-mh-32">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-v">内容</div>
	</div>
</div>

```html
<div class="bh-mv-8 bh-pv-8">内容</div>
mv = margin vertical，表示上下外边距
pv = padding vertical，表示上下内边距
```


<div class="bh-clearfix"></div>


<div class="boxmargin bh-mb-16 box-border-mp-t bh-mh-32">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-t">内容</div>
	</div>
</div>

```html
<div class="bh-mt-8 bh-pt-8">内容</div>
mt = margin top，表示底部外边距
pt = padding top，表示顶部内边距
```

<div class="bh-clearfix"></div>


<div class="boxmargin bh-mb-16 box-border-mp-b bh-mh-32">
	<div class="boxborder">
		<div class="boxpadding box-border-mp-b">内容</div>
	</div>
</div>

```html
<div class="bh-mb-8 bh-pb-8">内容</div>
mb = margin bottom，表示底部外边距
pb = padding bottom，表示底部内边距
```

<div class="bh-clearfix"></div>

除了以上组合外，你还可以随意组合，不过请注意，同一方向上的 margin 或 padding，最大值生效




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


## 边框

* .bh-border 添加边框
* .bh-border-h 添加左右边框
* .bh-border-l 添加左边框
* .bh-border-r 添加右边框
* .bh-border-v 添加上下边框
* .bh-border-t 添加上边框
* .bh-border-b 添加下边框

<div class="box bh-center-block bh-border-h bh-bColor-primary">文字</div>



## 浮动 & 清除浮动

使用浮动后，会使父容器高度为0，清除浮动后才可以占满空间

* .bh-clearfix 清除浮动
* .bh-clearfix-child 清除容器内子元素的浮动
* .bh-pull-left 左浮动
* .bh-pull-right 右浮动

### 未清除浮动的例子
<div class="bh-bg-info-3  bh-p-8">
  <button class="bh-btn bh-btn-default bh-pull-left">Example Button floated left</button>
  <button class="bh-btn bh-btn-default bh-pull-right">Example Button floated right</button>
</div>
我应该在第二行显示出来才对
<div class="bh-clearfix"></div>

```html
<div class="bh-bg-info-3 bh-p-8">
  <button class="bh-btn bh-btn-default bh-pull-left">Example Button floated left</button>
  <button class="bh-btn bh-btn-default bh-pull-right">Example Button floated right</button>
</div>
```

### 正确清除浮动的姿势
<div class="bh-bg-info-3 bh-clearfix bh-p-8">
  <button class="bh-btn bh-btn-default bh-pull-left">Example Button floated left</button>
  <button class="bh-btn bh-btn-default bh-pull-right">Example Button floated right</button>
</div>
应该在第二行显示出来才对

```html
<div class="bh-bg-info-3 bh-clearfix bh-p-8">
  <button class="bh-btn bh-btn-default bh-pull-left">Example Button floated left</button>
  <button class="bh-btn bh-btn-default bh-pull-right">Example Button floated right</button>
</div>
```


## 居中
* .bh-center-block 容器水平居中
* .bh-text-center 文字水平居中

内容需要有宽度才可以居中哦
<p>
	<div class="boxborder bh-center-block bh-text-center">文字</div>
</p>

```html
<div class="bh-center-block bh-text-center" style="width:120px">文字</div>
```



## 其他公共样式

* .bh-l-inline 将块级元素转成行内元素
* .bh-hide 隐藏元素
* .bh-show 显示元素
* .bh-str-cut 单行文字超长截断并出现点点点