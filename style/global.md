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
* bh-mh(margin horizontal缩写)表示左右外边距
* bh-mv(margin Vertical缩写)表示上下外边距
* bh-mb表示底部外边距
* bh-ph表示左右内边距
* bh-pv表示上下内边距
* bh-pt表示顶部内边距
* bh-pb表示底部内边距。




<table border="1" class="bh-text-center bh-text-caption">
    <tbody>
    <tr>
        <th>距离</th>
        <th>外边距</th>
        <th>左右外边距</th>
        <th>上下外边距</th>
        <th>底部外边距</th>
        <th>内边距</th>
        <th>左右内边距</th>
        <th>上下内边距</th>
        <th>顶部内边距</th>
        <th>底部内边距</th>
    </tr>
    <tr>
        <th>4px</th>
        <td>.bh-m-4</td>
        <td>.bh-mh-4</td>
        <td>.bh-mv-4</td>
        <td>.bh-mb-4</td>
        <td>.bh-p-4</td>
        <td>.bh-ph-4</td>
        <td>.bh-pv-4</td>
        <td>.bh-pt-4</td>
        <td>.bh-pb-4</td>
    </tr>
    <tr>
        <th>8px</th>
        <td>.bh-m-8</td>
        <td>.bh-mh-8</td>
        <td>.bh-mv-8</td>
        <td>.bh-mb-8</td>
        <td>.bh-p-8</td>
        <td>.bh-ph-8</td>
        <td>.bh-pv-8</td>
        <td>.bh-pt-8</td>
        <td>.bh-pb-8</td>
    </tr>
    <tr>
        <th>16px</th>
        <td>.bh-m-16</td>
        <td>.bh-mh-16</td>
        <td>.bh-mv-16</td>
        <td>.bh-mb-16</td>
        <td>.bh-p-16</td>
        <td>.bh-ph-16</td>
        <td>.bh-pv-16</td>
        <td>.bh-pt-16</td>
        <td>.bh-pb-16</td>
    </tr>
    <tr>
        <th>24px</th>
        <td>.bh-m-24</td>
        <td>.bh-mh-24</td>
        <td>.bh-mv-24</td>
        <td>.bh-mb-24</td>
        <td>.bh-p-24</td>
        <td>.bh-ph-24</td>
        <td>.bh-pv-24</td>
        <td>.bh-pt-24</td>
        <td>.bh-pb-24</td>
    </tr>
    <tr>
        <th>32px</th>
        <td>.bh-m-32</td>
        <td>.bh-mh-32</td>
        <td>.bh-mv-32</td>
        <td>.bh-mb-32</td>
        <td>.bh-p-32</td>
        <td>.bh-ph-32</td>
        <td>.bh-pv-32</td>
        <td>.bh-pt-32</td>
        <td>.bh-pb-32</td>
    </tr>
    </tbody>
</table>

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

