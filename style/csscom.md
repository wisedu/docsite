# 样式组件


<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">
<script type="text/javascript" src="http://res.wisedu.com/bower_components/jquery/dist/jquery.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bh-1.2.min.js"></script>

<style>
.book-summary{
	font-size:14px;
}
.bh-btn-grouped{
	margin-left: 4px;
	margin-right: 4px;
}
.fontsize12{
	font-size: 12px;
}
.panel{
    margin-bottom: 72px;
}
</style>


### 警告提示-alert

<p>
    <div class="bh-alert bh-alert-success">
       成功的提示文字
    </div>
    <div class="bh-alert bh-alert-warning">
        警告的提示文字
    </div>
    <div class="bh-alert bh-alert-danger">
        出错的提示文字
    </div>
</p>

<!--sec data-title="代码示例" data-id="section0" data-show=true data-collapse=true ces-->

```html
<div class="bh-alert bh-alert-success">
   成功的提示文字
</div>
<div class="bh-alert bh-alert-warning">
    警告的提示文字
</div>
<div class="bh-alert bh-alert-danger">
    出错的提示文字
</div>
```

<!--endsec-->

### 小圆

<p>
    <div class="bh-mb-16 scenes-circle-box bh-clearfix">
        <div class="bh-mh-8 sc-circle sc-circle-primary">1</div>
        <div class="bh-mh-8 sc-circle sc-circle-success">2</div>
        <div class="bh-mh-8 sc-circle sc-circle-info">3</div>
        <div class="bh-mh-8 sc-circle sc-circle-warning">4</div>
        <div class="bh-mh-8 sc-circle sc-circle-danger">5</div>
        <div class="bh-mh-8 sc-circle sc-circle-no">6</div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section1" data-show=true data-collapse=true ces-->

```html
<div class="bh-mh-8 sc-circle sc-circle-primary">1</div>
<div class="bh-mh-8 sc-circle sc-circle-success">2</div>
<div class="bh-mh-8 sc-circle sc-circle-info">3</div>
<div class="bh-mh-8 sc-circle sc-circle-warning">4</div>
<div class="bh-mh-8 sc-circle sc-circle-danger">5</div>
<div class="bh-mh-8 sc-circle sc-circle-no">6</div>
```

<!--endsec-->

### 标签 - bh-tag

<p>
    <div class="fontsize12">
    	<lable class="bh-tag bh-tag-primary">正方型</lable>
        <lable class="bh-tag bh-tag-success">正方型</lable>
        <lable class="bh-tag bh-tag-info">正方型</lable>
        <lable class="bh-tag bh-tag-warning">正方型</lable>
        <lable class="bh-tag bh-tag-danger">正方型</lable>
        <lable class="bh-tag bh-tag-round bh-tag-primary">椭圆形</lable>
        <lable class="bh-tag bh-tag-round bh-tag-success">椭圆形</lable>
        <lable class="bh-tag bh-tag-round bh-tag-info">椭圆形</lable>
        <lable class="bh-tag bh-tag-round bh-tag-warning">椭圆形</lable>
        <lable class="bh-tag bh-tag-round bh-tag-danger">椭圆形</lable>
        <lable class="bh-tag bh-tag-round bh-tag-default">椭圆形</lable>
    </div>
    <div class="bh-mv-16 fontsize12">
        <lable class="bh-tag bh-tag-primary bh-tag-active">
        	<span>标签2</span>
        	<i class="iconfont icon-close"></i>
        </lable>
        <label class="bh-tag bh-tag-round bh-tag-primary bh-tag-add">
        	<i class="iconfont icon-add"></i>
        </label>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section2" data-show=true data-collapse=true ces-->

```html
<lable class="bh-tag bh-tag-primary">正方型</lable>
<lable class="bh-tag bh-tag-success">正方型</lable>
<lable class="bh-tag bh-tag-info">正方型</lable>
<lable class="bh-tag bh-tag-warning">正方型</lable>
<lable class="bh-tag bh-tag-danger">正方型</lable>
<lable class="bh-tag bh-tag-round bh-tag-primary">椭圆形</lable>
<lable class="bh-tag bh-tag-round bh-tag-success">椭圆形</lable>
<lable class="bh-tag bh-tag-round bh-tag-info">椭圆形</lable>
<lable class="bh-tag bh-tag-round bh-tag-warning">椭圆形</lable>
<lable class="bh-tag bh-tag-round bh-tag-danger">椭圆形</lable>
<lable class="bh-tag bh-tag-round bh-tag-default">椭圆形</lable>

<lable class="bh-tag bh-tag-primary bh-tag-active">
	<span>标签2</span>
	<i class="iconfont icon-close"></i>
</lable>
<label class="bh-tag bh-tag-round bh-tag-primary bh-tag-add">
	<i class="iconfont icon-add"></i>
</label>
```

<!--endsec-->

### 按钮

#### 标准按钮

<p>
    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default bh-btn-large">Button</button>
        <button type="button" class="bh-btn bh-btn-primary bh-btn-large">Primary</button>
        <button type="button" class="bh-btn bh-btn-success bh-btn-large">Success</button>
        大号尺寸：.bh-btn-large
    </div>

    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default">Button</button>
        <button type="button" class="bh-btn bh-btn-primary">Primary</button>
        <button type="button" class="bh-btn bh-btn-success">Success</button>
        标准尺寸：不设置样式
    </div>

    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default bh-btn-small">Button</button>
        <button type="button" class="bh-btn bh-btn-primary bh-btn-small">Primary</button>
        <button type="button" class="bh-btn bh-btn-success bh-btn-small">Success</button>
        小号尺寸：.bh-btn-small
    </div>
</p>

<!--sec data-title="代码示例" data-id="section3" data-show=true data-collapse=true ces-->

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default bh-btn-large">Button</button>
    <button type="button" class="bh-btn bh-btn-primary ">Primary</button>
    <button type="button" class="bh-btn bh-btn-success bh-btn-small">Success</button>
</div>
```

<!--endsec-->

#### 禁用状态 Disable（所有普通按钮通用）

<p>
    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default" disabled onclick="alert('hello')">Disable</button>
        <button type="button" class="bh-btn bh-btn-primary" disabled >Primary</button>
        <button type="button" class="bh-btn bh-btn-success" disabled >Success</button>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section4" data-show=true data-collapse=true ces-->

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default" disabled onclick="alert('hello')">Disable</button>
    <button type="button" class="bh-btn bh-btn-primary" disabled >Primary</button>
    <button type="button" class="bh-btn bh-btn-success" disabled >Success</button>
</div>
```

<!--endsec-->

#### 带图标按钮

<p>
    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default bh-btn-large">
            <i class="iconfont icon-cameraalt"></i>Default</button>
        <button type="button" class="bh-btn bh-btn-primary bh-btn-large">
            <i class="iconfont icon-cameraalt"></i>Primary</button>
        <button type="button" class="bh-btn bh-btn-success bh-btn-large">
            <i class="iconfont icon-cameraalt"></i>Success</button>
        大号尺寸：.bh-btn-large
    </div>

    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default">
            <i class="iconfont icon-cameraalt"></i>Default</button>
        <button type="button" class="bh-btn bh-btn-primary">
            <i class="iconfont icon-cameraalt"></i>Primary</button>
        <button type="button" class="bh-btn bh-btn-success">
            <i class="iconfont icon-cameraalt"></i>Success</button>
        标准尺寸：不设置样式
    </div>

    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default bh-btn-small">
            <i class="iconfont icon-cameraalt"></i>Default</button>
        <button type="button" class="bh-btn bh-btn-primary bh-btn-small">
            <i class="iconfont icon-cameraalt"></i>Primary</button>
        <button type="button" class="bh-btn bh-btn-success bh-btn-small">
            <i class="iconfont icon-cameraalt"></i>Success</button>
        小号尺寸：.bh-btn-small
    </div>
</p>

<!--sec data-title="代码示例" data-id="section5" data-show=true data-collapse=true ces-->

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default bh-btn-large">
        <i class="iconfont icon-cameraalt"></i>Default</button>
    <button type="button" class="bh-btn bh-btn-primary">
        <i class="iconfont icon-cameraalt"></i>Primary</button>
    <button type="button" class="bh-btn bh-btn-success bh-btn-small">
        <i class="iconfont icon-cameraalt"></i>Success</button>
</div>
```

<!--endsec-->

#### 圆形按钮

<p>
    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-circle bh-btn-primary">
            <i class="iconfont icon-check"></i>
        </button>
        <button type="button" class="bh-btn bh-btn-circle bh-btn-success">
            <i class="iconfont icon-check"></i>
        </button>
        <button type="button" class="bh-btn bh-btn-circle bh-btn-default">
            <i class="iconfont icon-close"></i>
        </button>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section6" data-show=true data-collapse=true ces-->

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-circle bh-btn-primary">
        <i class="iconfont icon-check"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-circle bh-btn-success">
        <i class="iconfont icon-check"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-circle bh-btn-default">
        <i class="iconfont icon-close"></i>
    </button>
</div>
```

<!--endsec-->

#### 卡片操作按钮

<p>
    <div class="bh-btn-grouped">
        <button type="button" class="bh-btn bh-btn-default bh-btn-small bh-btn-icon">
            <i class="iconfont icon-close"></i>
        </button>
        <button type="button" class="bh-btn bh-btn-default bh-btn-small bh-btn-icon bh-disabled">
            <i class="iconfont icon-close"></i>
        </button>

        <button type="button" class="bh-btn bh-btn-primary bh-btn-icon">
            <i class="iconfont icon-close"></i>
        </button>
        <button type="button" class="bh-btn bh-btn-primary bh-btn-icon bh-disabled">
            <i class="iconfont icon-close"></i>
        </button>

        <button type="button" class="bh-btn bh-btn-success bh-btn-large bh-btn-icon">
            <i class="iconfont icon-close"></i>
        </button>
        <button type="button" class="bh-btn bh-btn-success bh-btn-large bh-btn-icon bh-disabled">
            <i class="iconfont icon-close"></i>
        </button>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section7" data-show=true data-collapse=true ces-->

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default bh-btn-small bh-btn-icon">
        <i class="iconfont icon-close"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-default bh-btn-small bh-btn-icon bh-disabled">
        <i class="iconfont icon-close"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-primary bh-btn-icon">
        <i class="iconfont icon-close"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-primary bh-btn-icon bh-disabled">
        <i class="iconfont icon-close"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-success bh-btn-large bh-btn-icon">
        <i class="iconfont icon-close"></i>
    </button>
    <button type="button" class="bh-btn bh-btn-success bh-btn-large bh-btn-icon bh-disabled">
        <i class="iconfont icon-close"></i>
    </button>
</div>
```

<!--endsec-->

#### 左右按钮分组

<p>
    <div class="bh-btn-grouped">
        <div class="bh-pull-left">
            <button type="button" class="bh-btn bh-btn-default">导出</button>
            <button type="button" class="bh-btn bh-btn-default">导入</button>
        </div>
        <div class="bh-pull-right">
            <button type="button" class="bh-btn bh-btn-default bh-btn-icon"><i class="iconfont"></i></button>
            <button type="button" class="bh-btn bh-btn-default bh-btn-icon"><i class="iconfont"></i></button>
            <button type="button" class="bh-btn bh-btn-default"><i class="iconfont"></i>自定义显示列</button>
            <button type="button" class="bh-btn bh-btn-default"><i class="iconfont"></i>查看统计</button>
        </div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section8" data-show=true data-collapse=true ces-->

```html
<div class="bh-btn-grouped">
    <div class="bh-pull-left">
        <button type="button" class="bh-btn bh-btn-default">导出</button>
        <button type="button" class="bh-btn bh-btn-default">导入</button>
    </div>
    <div class="bh-pull-right">
        <button type="button" class="bh-btn bh-btn-default bh-btn-icon"><i class="iconfont"></i></button>
        <button type="button" class="bh-btn bh-btn-default bh-btn-icon"><i class="iconfont"></i></button>
        <button type="button" class="bh-btn bh-btn-default"><i class="iconfont"></i>自定义显示列</button>
        <button type="button" class="bh-btn bh-btn-default"><i class="iconfont"></i>查看统计</button>
    </div>
</div>
```

<!--endsec-->

### 分页样式

<p>
	<div class="clearfix" style="margin-bottom: 24px;">
        <ul class="bh-pagination bh-pull-left">
            <li class="bh-disabled">
                <a href="javascript:void(0)" aria-label="Previous">
                    <span aria-hidden="true">«</span>
                </a>
            </li>
            <li><a href="javascript:void(0)">1</a></li>
            <li class="bh-disabled"><a href="javascript:void(0)">2</a></li>
            <li><a href="javascript:void(0)">3</a></li>
            <li class="bh-active"><a href="javascript:void(0)">4</a></li>
            <li><a href="javascript:void(0)">5</a></li>
            <li>
                <a href="javascript:void(0)" aria-label="Next">
                    <span aria-hidden="true">»</span>
                </a>
            </li>
        </ul>
        <div class="bh-pagination-skip bh-pull-left">
            <span class="bh-pull-left bh-mv-2">跳转至</span><input type="text" class="bh-form-control bh-pull-left"><span class="bh-pull-left bh-mv-2">页</span>
            <a class="bh-btn bh-btn-default bh-btn-xs">GO</a>
        </div>

        <div class="bh-pagination-total bh-pull-right">
            共9页，88条记录，每页显示<select class="bh-form-control">
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="20">20</option>
        </select>条
        </div>
        <div class="bh-clearfix"></div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section9" data-show=true data-collapse=true ces-->

```html
<div class="clearfix bh-mb-24">
    <ul class="bh-pagination bh-pull-left">
        <li class="bh-disabled">
            <a href="javascript:void(0)" aria-label="Previous">
                <span aria-hidden="true">«</span>
            </a>
        </li>
        <li><a href="javascript:void(0)">1</a></li>
        <li class="bh-disabled"><a href="javascript:void(0)">2</a></li>
        <li><a href="javascript:void(0)">3</a></li>
        <li class="bh-active"><a href="javascript:void(0)">4</a></li>
        <li><a href="javascript:void(0)">5</a></li>
        <li>
            <a href="javascript:void(0)" aria-label="Next">
                <span aria-hidden="true">»</span>
            </a>
        </li>
    </ul>
    <div class="bh-pagination-skip bh-pull-left">
        <span class="bh-pull-left bh-mv-2">跳转至</span><input type="text" class="bh-form-control bh-pull-left"><span class="bh-pull-left bh-mv-2">页</span>
        <a class="bh-btn bh-btn-default bh-btn-xs">GO</a>
    </div>
    <div class="bh-pagination-total bh-pull-right">
        共9页，88条记录，每页显示<select class="bh-form-control">
        <option value="5">5</option>
        <option value="10">10</option>
        <option value="20">20</option>
    </select>条
    </div>
    <div class="bh-clearfix"></div>
</div>
```

<!--endsec-->


### 下拉菜单 - Dropdown

<p>
    <div class="bh-btn-grouped">
    	<div class="bh-dropdown" bh-dropdown-role="bhDropdown">
    	    <button class="bh-btn bh-btn-default bh-btn-larger" type="button" bh-dropdown-role="bhDropdownBtn" >
    	        默认状态
    	    </button>
    	    <ul class="bh-dropdown-menu" bh-dropdown-role="bhDropdownMenu">
    	        <li><a href="javascript:void(0)">Action</a></li>
    	        <li class="bh-disabled"><a href="javascript:void(0)">Another action</a></li>
    	        <li><a href="javascript:void(0)">Something else here</a></li>
    	        <li><a href="javascript:void(0)">Something else here</a></li>
    	        <li class="bh-dropdown-divider"></li>
    	        <li><a href="javascript:void(0)">Separated link</a></li>
    	    </ul>
    	</div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section10" data-show=true data-collapse=true ces-->

```html
<div class="bh-dropdown" bh-dropdown-role="bhDropdown">
    <button class="bh-btn bh-btn-default bh-btn-larger" type="button" bh-dropdown-role="bhDropdownBtn" >
        默认状态
    </button>
    <ul class="bh-dropdown-menu" bh-dropdown-role="bhDropdownMenu">
        <li><a href="javascript:void(0)">Action</a></li>
        <li class="bh-disabled"><a href="javascript:void(0)">Another action</a></li>
        <li><a href="javascript:void(0)">Something else here</a></li>
        <li><a href="javascript:void(0)">Something else here</a></li>
        <li class="bh-dropdown-divider"></li>
        <li><a href="javascript:void(0)">Separated link</a></li>
    </ul>
</div>
```

<!--endsec-->

<p>
    <div class="bh-btn-grouped">
    	<div class="bh-dropdown bh-dropdown-primary bh-dropdown-right bh-clearfix" bh-dropdown-role="bhDropdown">
    	    <button class="bh-btn bh-btn-default bh-btn-small bh-btn-primary" type="button" bh-dropdown-role="bhDropdownBtn" >
    	        <i class="iconfont icon-add"></i>
    	        从右上角展开状态
    	    </button>
    	    <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
    	        <li><a href="javascript:void(0)">Action</a></li>
    	        <li class="bh-disabled"><a href="javascript:void(0)">Another action</a></li>
    	        <li><a href="javascript:void(0)">Something else here</a></li>
    	        <li><a href="javascript:void(0)">Something else here</a></li>
    	        <li class="bh-dropdown-divider"></li>
    	        <li><a href="javascript:void(0)">Separated link</a></li>
    	    </ul>
    	</div>
    </div>
</p>

设置该样式，使其展开：bh-dropdown-open

<!--sec data-title="代码示例" data-id="section11" data-show=true data-collapse=true ces-->

```html
<div class="bh-dropdown bh-dropdown-primary bh-dropdown-right bh-clearfix" bh-dropdown-role="bhDropdown">
    <button class="bh-btn bh-btn-default bh-btn-small bh-btn-primary" type="button" bh-dropdown-role="bhDropdownBtn" >
        <i class="iconfont icon-add"></i>
        从右上角展开状态
    </button>
    <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
        ...
    </ul>
</div>
```

<!--endsec-->

<p>
    <div class="bh-btn-grouped">
        <div class="bh-dropdown bh-dropdown-up" bh-dropdown-role="bhDropdown">
            <button class="bh-btn bh-btn-default" type="button" bh-dropdown-role="bhDropdownBtn" >
                <i class="iconfont icon-add"></i>
                从左下角展开状态
            </button>
            <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
                <li><a href="javascript:void(0)">Action</a></li>
                <li class="bh-disabled"><a href="javascript:void(0)">Another action</a></li>
                <li><a href="javascript:void(0)">Something else here</a></li>
                <li><a href="javascript:void(0)">Something else here</a></li>
                <li class="bh-dropdown-divider"></li>
                <li><a href="javascript:void(0)">Separated link</a></li>
            </ul>
        </div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section12" data-show=true data-collapse=true ces-->

```html
<div class="bh-dropdown bh-dropdown-up" bh-dropdown-role="bhDropdown">
    ...
</div>

```

<!--endsec-->

<p>
    <div class="bh-btn-grouped">
        <div class="bh-dropdown bh-dropdown-right-up" bh-dropdown-role="bhDropdown">
            <button class="bh-btn bh-btn-default" type="button" bh-dropdown-role="bhDropdownBtn" >
                <i class="iconfont icon-add"></i>
                Drop
            </button>
            <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
                <li><a href="javascript:void(0)">Action</a></li>
                <li class="bh-disabled"><a href="javascript:void(0)">Another action</a></li>
                <li><a href="javascript:void(0)">Something else here</a></li>
                <li><a href="javascript:void(0)">Something else here</a></li>
                <li class="bh-dropdown-divider"></li>
                <li><a href="javascript:void(0)">Separated link</a></li>
            </ul>
        </div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section13" data-show=true data-collapse=true ces-->

```html
<div class="bh-dropdown bh-dropdown-right-up" bh-dropdown-role="bhDropdown">
    ...
</div>
```

<!--endsec-->



### 纯html折叠面板 flex-panel

<p>
	<div bh-flex-panel-role="flex-panel">
		<div bh-flex-panel-role="panel-title">
			<h3>flex-panel-title</h3>
		</div>
		<div bh-flex-panel-role="panel-content-wrap" style="height:0">
			<div bh-flex-panel-role="panel-content">
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
				<p>flex-panel-content</p>
			</div>
		</div>
	</div>
</p>

<!--sec data-title="代码示例" data-id="section14" data-show=true data-collapse=true ces-->

```html
<div bh-flex-panel-role="flex-panel">
	<div bh-flex-panel-role="panel-title">
		<h3>flex-panel-title</h3>
	</div>
	<div bh-flex-panel-role="panel-content-wrap" style="height:0">
		<div bh-flex-panel-role="panel-content">
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
			<p>flex-panel-content</p>
		</div>
	</div>
</div>
```

<!--endsec-->
