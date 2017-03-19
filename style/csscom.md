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
</style>


### 警告提示-alert

<div class="bh-alert bh-alert-success">
   成功的提示文字
</div>
<div class="bh-alert bh-alert-warning">
    警告的提示文字
</div>
<div class="bh-alert bh-alert-danger">
    出错的提示文字
</div>

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

### 小圆

<div class="bh-mb-16 scenes-circle-box bh-clearfix">
    <div class="bh-mh-8 sc-circle sc-circle-primary">1</div>
    <div class="bh-mh-8 sc-circle sc-circle-success">2</div>
    <div class="bh-mh-8 sc-circle sc-circle-info">3</div>
    <div class="bh-mh-8 sc-circle sc-circle-warning">4</div>
    <div class="bh-mh-8 sc-circle sc-circle-danger">5</div>
    <div class="bh-mh-8 sc-circle sc-circle-no">6</div>
</div>

```html
<div class="bh-mh-8 sc-circle sc-circle-primary">1</div>
<div class="bh-mh-8 sc-circle sc-circle-success">2</div>
<div class="bh-mh-8 sc-circle sc-circle-info">3</div>
<div class="bh-mh-8 sc-circle sc-circle-warning">4</div>
<div class="bh-mh-8 sc-circle sc-circle-danger">5</div>
<div class="bh-mh-8 sc-circle sc-circle-no">6</div>
```

### 标签 - bh-tag

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

### 按钮

#### 标准按钮

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

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default bh-btn-large">Button</button>
    <button type="button" class="bh-btn bh-btn-primary ">Primary</button>
    <button type="button" class="bh-btn bh-btn-success bh-btn-small">Success</button>
</div>
```

#### 禁用状态 Disable（所有普通按钮通用）

<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default" disabled onclick="alert('hello')">Disable</button>
    <button type="button" class="bh-btn bh-btn-primary" disabled >Primary</button>
    <button type="button" class="bh-btn bh-btn-success" disabled >Success</button>
</div>

```html
<div class="bh-btn-grouped">
    <button type="button" class="bh-btn bh-btn-default" disabled onclick="alert('hello')">Disable</button>
    <button type="button" class="bh-btn bh-btn-primary" disabled >Primary</button>
    <button type="button" class="bh-btn bh-btn-success" disabled >Success</button>
</div>
```

#### 带图标按钮

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

#### 圆形按钮

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

#### 卡片操作按钮

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

#### 左右按钮分组

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

### 单选
#### radio 单例 普通、不可用、已选不可用

<div class="fontsize12">
    <div class="bh-radio">
        <label class="bh-radio-label">
            <input type="radio" name="SHHD" value="0" data-caption="考察干部">
            <i class="bh-choice-helper"></i>
            考察干部
        </label>
    </div>
    <div class="bh-radio">
        <label class="bh-radio-label" >
            <input type="radio" name="SHHD" disabled value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            关心下一代
        </label>
    </div>
    <div class="bh-radio">
        <label class="bh-radio-label" >
            <input type="radio" name="SHHD" disabled checked value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            关心下一代
        </label>
    </div>
</div>

```html
<div class="bh-radio">
    <label class="bh-radio-label">
        <input type="radio" name="SHHD" value="0" data-caption="考察干部">
        <i class="bh-choice-helper"></i>
        考察干部
    </label>
</div>
<div class="bh-radio">
    <label class="bh-radio-label">
        <input type="radio" name="SHHD" disabled value="1" data-caption="关心下一代">
        <i class="bh-choice-helper"></i>
        关心下一代
    </label>
</div>
<div class="bh-radio">
    <label class="bh-radio-label">
        <input type="radio" name="SHHD" disabled checked value="1" data-caption="关心下一代">
        <i class="bh-choice-helper"></i>
        关心下一代
    </label>
</div>
```

#### radio group 横向排列

<div class="fontsize12">
    <div class="bh-radio bh-radio-group-h">
        <label class="bh-radio-label">
            <input type="radio" name="nl" value="0" data-caption="考察干部">
            <i class="bh-choice-helper"></i>
            考察干部
        </label>
        <label class="bh-radio-label" >
            <input type="radio" name="nl" disabled value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            关心下一代
        </label>
        <label class="bh-radio-label" >
            <input type="radio" name="nl" disabled checked value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            关心下一代
        </label>
    </div>
</div>

```html
<div class="bh-radio bh-radio-group-h">
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
</div>
```

#### radio group 竖直排列

<div class="fontsize12">
    <div class="bh-radio bh-radio-group-v">
        <label class="bh-radio-label">
            <input type="radio" name="SHHD_V" value="0" data-caption="考察干部">
            <i class="bh-choice-helper"></i>
            考察干部
        </label>
    
        <label class="bh-radio-label" >
            <input type="radio" name="SHHD_V" disabled value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            关心下一代
        </label>
    
        <label class="bh-radio-label" >
            <input type="radio" name="SHHD_V" disabled checked value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            关心下一代
        </label>
    </div>
</div>

```html
<div class="bh-radio bh-radio-group-v">
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
</div>
```



### 多选 - bh-checkbox

#### checkbox 单例 普通、不可用、已选不可用

<div class="fontsize12">
    <div class="bh-checkbox">
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" value="0" data-caption="考察干部">
            <i class="bh-choice-helper"></i>
            可选
        </label>
    </div>
    <div class="bh-checkbox">
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" value="1" disabled data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            不可用
        </label>
    </div>
    <div class="bh-checkbox">
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" value="1" disabled checked data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            已选、不可用
        </label>
    </div>
</div>

```html
<div class="bh-checkbox">
    <label class="bh-checkbox-label">
        <input type="checkbox" name="SHHD" value="0" data-caption="考察干部">
        <i class="bh-choice-helper"></i>
        可选
    </label>
</div>
<div class="bh-checkbox">
    <label class="bh-checkbox-label">
        <input type="checkbox" name="SHHD" value="1" disabled data-caption="关心下一代">
        <i class="bh-choice-helper"></i>
        不可用
    </label>
</div>
<div class="bh-checkbox">
    <label class="bh-checkbox-label">
        <input type="checkbox" name="SHHD" value="1" disabled checked data-caption="关心下一代">
        <i class="bh-choice-helper"></i>
        已选、不可用
    </label>
</div>
```

#### checkbox group 水平排列

<div class="fontsize12">
    <div class="bh-checkbox bh-checkbox-group-h">
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" value="0" data-caption="考察干部">
            <i class="bh-choice-helper"></i>
            可选
        </label>
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" disabled value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            不可用
        </label>
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" disabled checked value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            已选、不可用
        </label>
    </div>
</div>

```html
<div class="bh-checkbox bh-checkbox-group-h">
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
</div>
```

#### checkbox group 竖直排列

<div class="fontsize12">
    <div class="bh-checkbox bh-checkbox-group-v">
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" value="0" data-caption="考察干部">
            <i class="bh-choice-helper"></i>
            可选
        </label>
    
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" disabled="" value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            不可用
        </label>
    
        <label class="bh-checkbox-label">
            <input type="checkbox" name="SHHD" disabled="" checked="" value="1" data-caption="关心下一代">
            <i class="bh-choice-helper"></i>
            已选、不可用
        </label>
    </div>
</div>

```html
<div class="bh-checkbox bh-checkbox-group-v">
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
</div>
```


### 开关 - bh-switch

<div class="bh-switch fontsize12">
    <label class="bh-switch-label">默认</label>
    <input type="checkbox">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>

<div class="bh-switch fontsize12">
    <label class="bh-switch-label">默认打开</label>
    <input type="checkbox" checked="">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>


<div class="bh-switch fontsize12">
    <label class="bh-switch-label">禁用</label>
    <input type="checkbox" disabled="">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>

<div class="bh-switch fontsize12">
    <label class="bh-switch-label">禁用打开</label>
    <input type="checkbox" disabled="" checked="">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>

```html
<div class="bh-switch">
    <label class="bh-switch-label">默认</label>
    <input type="checkbox">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>
<div class="bh-switch">
    <label class="bh-switch-label">默认打开</label>
    <input type="checkbox" checked="">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>
<div class="bh-switch">
    <label class="bh-switch-label">禁用</label>
    <input type="checkbox" disabled="">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>
<div class="bh-switch">
    <label class="bh-switch-label">禁用打开</label>
    <input type="checkbox" disabled="" checked="">
    <label class="bh-switch-helper"></label>
    <label class="bh-switch-text" open-text="打开" close-text="关闭"></label>
</div>
```


### 分页样式

<p>
	<div class="clearfix" style="margin-bottom: 24px;">
        <ul class="bh-pagination bh-pull-left">
            <li class="bh-disabled">
                <a href="#" aria-label="Previous">
                    <span aria-hidden="true">«</span>
                </a>
            </li>
            <li><a href="#">1</a></li>
            <li class="bh-disabled"><a href="#">2</a></li>
            <li><a href="#">3</a></li>
            <li class="bh-active"><a href="#">4</a></li>
            <li><a href="#">5</a></li>
            <li>
                <a href="#" aria-label="Next">
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

```html
<div class="clearfix bh-mb-24">
    <ul class="bh-pagination bh-pull-left">
        <li class="bh-disabled">
            <a href="#" aria-label="Previous">
                <span aria-hidden="true">«</span>
            </a>
        </li>
        <li><a href="#">1</a></li>
        <li class="bh-disabled"><a href="#">2</a></li>
        <li><a href="#">3</a></li>
        <li class="bh-active"><a href="#">4</a></li>
        <li><a href="#">5</a></li>
        <li>
            <a href="#" aria-label="Next">
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


### 下拉菜单 - Dropdown

<div class="bh-btn-grouped">
	<div class="bh-dropdown" bh-dropdown-role="bhDropdown">
	    <button class="bh-btn bh-btn-default bh-btn-larger" type="button" bh-dropdown-role="bhDropdownBtn" >
	        默认状态
	    </button>
	    <ul class="bh-dropdown-menu" bh-dropdown-role="bhDropdownMenu">
	        <li><a href="#">Action</a></li>
	        <li class="bh-disabled"><a href="#">Another action</a></li>
	        <li><a href="#">Something else here</a></li>
	        <li><a href="#">Something else here</a></li>
	        <li class="bh-dropdown-divider"></li>
	        <li><a href="#">Separated link</a></li>
	    </ul>
	</div>
</div>

```html
<div class="bh-dropdown" bh-dropdown-role="bhDropdown">
    <button class="bh-btn bh-btn-default bh-btn-larger" type="button" bh-dropdown-role="bhDropdownBtn" >
        默认状态
    </button>
    <ul class="bh-dropdown-menu" bh-dropdown-role="bhDropdownMenu">
        <li><a href="#">Action</a></li>
        <li class="bh-disabled"><a href="#">Another action</a></li>
        <li><a href="#">Something else here</a></li>
        <li><a href="#">Something else here</a></li>
        <li class="bh-dropdown-divider"></li>
        <li><a href="#">Separated link</a></li>
    </ul>
</div>
```

<div class="bh-btn-grouped">
	<div class="bh-dropdown bh-dropdown-primary bh-dropdown-right bh-clearfix" bh-dropdown-role="bhDropdown">
	    <button class="bh-btn bh-btn-default bh-btn-small bh-btn-primary" type="button" bh-dropdown-role="bhDropdownBtn" >
	        <i class="iconfont icon-add"></i>
	        从右上角展开状态
	    </button>
	    <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
	        <li><a href="#">Action</a></li>
	        <li class="bh-disabled"><a href="#">Another action</a></li>
	        <li><a href="#">Something else here</a></li>
	        <li><a href="#">Something else here</a></li>
	        <li class="bh-dropdown-divider"></li>
	        <li><a href="#">Separated link</a></li>
	    </ul>
	</div>
</div>

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
设置该样式，使其展开：bh-dropdown-open
```

<div class="bh-btn-grouped">
    <div class="bh-dropdown bh-dropdown-up" bh-dropdown-role="bhDropdown">
        <button class="bh-btn bh-btn-default" type="button" bh-dropdown-role="bhDropdownBtn" >
            <i class="iconfont icon-add"></i>
            从左下角展开状态
        </button>
        <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
            <li><a href="#">Action</a></li>
            <li class="bh-disabled"><a href="#">Another action</a></li>
            <li><a href="#">Something else here</a></li>
            <li><a href="#">Something else here</a></li>
            <li class="bh-dropdown-divider"></li>
            <li><a href="#">Separated link</a></li>
        </ul>
    </div>
</div>

```html
<div class="bh-dropdown bh-dropdown-up" bh-dropdown-role="bhDropdown">
    ...
</div>

```
<div class="bh-btn-grouped">
    <div class="bh-dropdown bh-dropdown-right-up" bh-dropdown-role="bhDropdown">
        <button class="bh-btn bh-btn-default" type="button" bh-dropdown-role="bhDropdownBtn" >
            <i class="iconfont icon-add"></i>
            Drop
        </button>
        <ul class="bh-dropdown-menu bh-dropdown-open" bh-dropdown-role="bhDropdownMenu">
            <li><a href="#">Action</a></li>
            <li class="bh-disabled"><a href="#">Another action</a></li>
            <li><a href="#">Something else here</a></li>
            <li><a href="#">Something else here</a></li>
            <li class="bh-dropdown-divider"></li>
            <li><a href="#">Separated link</a></li>
        </ul>
    </div>
</div>

```html
<div class="bh-dropdown bh-dropdown-right-up" bh-dropdown-role="bhDropdown">
    ...
</div>
```
