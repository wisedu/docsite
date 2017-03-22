# 布局

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<style>
.book-summary{
	font-size:14px;
}
.grid-system > .bh-row{
	border: 1px solid #ddd;
}
.grid-system > .bh-row > div:not(:last-child){
	border-right: 1px solid #ddd;
}
.grid-system > .bh-row:not(:first-child){
	border-top: none;
}
</style>

### 栅格系统

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

<!--sec data-title="代码示例" data-id="section0" data-show=true data-collapse=true ces-->

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

<!--endsec-->

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
		</div>
	</div>
</p>

