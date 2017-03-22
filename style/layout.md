# 布局

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<style>
.book-summary{
	font-size:14px;
}
[class|=bh-col-md]{
	border:1px solid #ddd;
	background-color: #F0F1F9;
}
.panel{
    margin-bottom: 72px;
}
</style>

### 栅格系统

系统会自动分为最多12列

<p>
	<div class="grid-system">
        <div class="bh-row">
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
            <div class="bh-col-md-1">.bh-col-md-1</div>
        </div>
        <div class="bh-row">
            <div class="bh-col-md-8">.bh-col-md-8</div>
            <div class="bh-col-md-4">.bh-col-md-4</div>
        </div>
        <div class="bh-row">
            <div class="bh-col-md-4">.bh-col-md-4</div>
            <div class="bh-col-md-4">.bh-col-md-4</div>
            <div class="bh-col-md-4">.bh-col-md-4</div>
        </div>
        <div class="bh-row">
            <div class="bh-col-md-6">.bh-col-md-6</div>
            <div class="bh-col-md-6">.bh-col-md-6</div>
        </div>
    </div>
</p>

使用单一的一组 .bh-col-md-* 栅格类，就可以创建一个基本的栅格系统，所有“列（column）必须放在 ” .bh-row 内。

```html
<div class="bh-row">
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
    <div class="bh-col-md-1">.bh-col-md-1</div>
</div>
<div class="bh-row">
    <div class="bh-col-md-8">.bh-col-md-8</div>
    <div class="bh-col-md-4">.bh-col-md-4</div>
</div>
<div class="bh-row">
    <div class="bh-col-md-4">.bh-col-md-4</div>
    <div class="bh-col-md-4">.bh-col-md-4</div>
    <div class="bh-col-md-4">.bh-col-md-4</div>
</div>
<div class="bh-row">
    <div class="bh-col-md-6">.bh-col-md-6</div>
    <div class="bh-col-md-6">.bh-col-md-6</div>
</div>
</div>
```


### 嵌套列

<p>
	<div class="grid-system">
		<div class="bh-row">
		  <div class="bh-col-md-9">
		    Level 1: .bh-col-md-9
		    <div class="bh-row">
		      <div class="bh-col-md-6">
		        Level 2: .bh-col-md-6
		      </div>
		      <div class="bh-col-md-6">
		        Level 2: .bh-col-md-6
		      </div>
		    </div>
		  </div>
		  <div class="bh-col-md-3">Level 1: .bh-col-md-3</div>
		</div>
	</div>
</p>

为了使用内置的栅格系统将内容再次嵌套，可以通过添加一个新的 .bh-row 元素和一系列 .bh-col-md-* 元素到已经存在的 .col-md-* 元素内。被嵌套的行（row）所包含的列（column）的个数不能超过12（其实，没有要求你必须占满12列）。

```html
<div class="bh-row">
  <div class="bh-col-md-9">
    Level 1: .bh-col-md-9
    <div class="bh-row">
      <div class="bh-col-md-6">
        Level 2: .bh-col-md-6
      </div>
      <div class="bh-col-md-6">
        Level 2: .bh-col-md-6
      </div>
    </div>
  </div>
  <div class="bh-col-md-3">Level 1: .bh-col-md-3</div>
</div>
```

### 多余的列（column）将另起一行排列

<p>
	<div class="grid-system">
		<div class="bh-row">
		  <div class="bh-col-md-9">.bh-col-md-9</div>
		  <div class="bh-col-md-4">.bh-col-md-4<br>Since 9 + 4 = 13 &gt; 12, this 4-column-wide div gets wrapped onto a new line as one contiguous unit.</div>
		  <div class="bh-col-md-6">.bh-col-md-6<br>Subsequent columns continue along the new line.</div>
		</div>
	</div>
</p>

如果在一个 .row 内包含的列（column）大于12个，包含多余列（column）的元素将作为一个整体单元被另起一行排列。

```html
<div class="bh-row">
  <div class="bh-col-md-9">.bh-col-md-9</div>
  <div class="bh-col-md-4">.bh-col-md-4<br>Since 9 + 4 = 13 &gt; 12, this 4-column-wide div gets wrapped onto a new line as one contiguous unit.</div>
  <div class="bh-col-md-6">.bh-col-md-6<br>Subsequent columns continue along the new line.</div>
</div>
```