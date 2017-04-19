# 表单样式

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">

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

### 输入组件

<p>
    <form class="bh-form-vertical fontsize12 bh-clearfix">
        <div class="bh-form-group bh-col-md-8 bh-required">
            <label class="bh-form-label">字段名称：</label>
            <div>
                <input type="text" class="bh-form-control" placeholder="提示文字">
            </div>
        </div>
        <div class="bh-form-group bh-col-md-8">
            <label class="bh-form-label">字段名称：</label>
            <div>
                <select class="bh-form-control">
                	<option>第一项</option>
                	<option>第二项</option>
                </select>
            </div>
        </div>
        <div class="bh-form-group bh-col-md-8">
            <label class="bh-form-label">字段名称：</label>
            <div>
                <select class="bh-form-control" multiple style="height: 50px">
                	<option>第一项</option>
                	<option>第二项</option>
                </select>
            </div>
        </div>
        <div class="bh-form-group bh-col-md-8 bh-required">
            <label class="bh-form-label">字段名称：</label>
            <div class="bh-form-control-warning">
                <input type="text" class="bh-form-control" disabled placeholder="提示文字">
                <div class="bh-text-caption bh-color-warning"><i class="md md-warning"></i>警告提示文字</div>
            </div>
        </div>
        <div class="bh-form-group bh-col-md-8 bh-required">
            <label class="bh-form-label">字段名称：</label>
            <div class="bh-form-control-danger">
                <input type="text" class="bh-form-control" readonly placeholder="提示文字">
                <div class="bh-text-caption bh-color-danger"><i class="md md-warning"></i>错误提示文字</div>
            </div>
        </div>
        <div class="bh-form-group bh-col-md-8">
            <label class="bh-form-label">字段名称：</label>
            <div>
                <textarea class="bh-form-control" rows="3" placeholder="提示文字"></textarea>
            </div>
        </div>
    </form>
</p>

<!--sec data-title="代码示例" data-id="section0" data-show=true data-collapse=true ces-->

```html
<input type="text" class="bh-form-control" disabled placeholder="提示文字">
<input type="text" class="bh-form-control" readonly placeholder="提示文字">
<select class="bh-form-control">
	<option>第一项</option>
	<option>第二项</option>
</select>
<select class="bh-form-control" multiple style="height: 50px">
	<option>第一项</option>
	<option>第二项</option>
</select>
<textarea class="bh-form-control" rows="3" placeholder="提示文字"></textarea>
```

<!--endsec-->

#### 后缀

<p>
    <div class="bh-input-group fontsize12">
        <input type="text" class="bh-form-control" placeholder="Username">
        <div class="bh-input-group-addon">万</div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section1" data-show=true data-collapse=true ces-->

```html
<div class="bh-input-group">
    <input type="text" class="bh-form-control" placeholder="Username">
    <div class="bh-input-group-addon">万</div>
</div>
```

<!--endsec-->

### 单选
#### radio 单例 普通、不可用、已选不可用

<p>
    <div class="fontsize12">
        <div class="bh-radio">
            <label class="bh-radio-label">
                <input type="radio" name="single1" value="0" data-caption="我是一个普通的radio">
                <i class="bh-choice-helper"></i>
                我是一个普通的radio
            </label>
        </div>
        <div class="bh-radio">
            <label class="bh-radio-label" >
                <input type="radio" name="single2" disabled value="1" data-caption="我是一个不可用的radio，默认状态为未选中">
                <i class="bh-choice-helper"></i>
                我是一个不可用的radio，默认状态为未选中
            </label>
        </div>
        <div class="bh-radio">
            <label class="bh-radio-label" >
                <input type="radio" name="single3" disabled checked value="1" data-caption="我是一个不可用的radio，默认状态为选中！">
                <i class="bh-choice-helper"></i>
                我是一个不可用的radio，默认状态为选中！
            </label>
        </div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section2" data-show=true data-collapse=true ces-->

```html
<div class="bh-radio">

            <label class="bh-radio-label">

                <input type="radio" name="single1" value="0" data-caption="我是一个普通的radio">

                <i class="bh-choice-helper"></i>

                我是一个普通的radio

            </label>

        </div>

        <div class="bh-radio">

            <label class="bh-radio-label" >

                <input type="radio" name="single2" disabled value="1" data-caption="我是一个不可用的radio，默认状态为未选中">

                <i class="bh-choice-helper"></i>

                我是一个不可用的radio，默认状态为未选中

            </label>

        </div>

        <div class="bh-radio">

            <label class="bh-radio-label" >

                <input type="radio" name="single3" disabled checked value="1" data-caption="我是一个不可用的radio，默认状态为选中！">

                <i class="bh-choice-helper"></i>

                我是一个不可用的radio，默认状态为选中！

            </label>

        </div>
```

<!--endsec-->

#### radio group 横向排列

<p>
    <div class="fontsize12">
        <div class="bh-radio bh-radio-group-h">
            <label class="bh-radio-label">
                <input type="radio" name="nl" value="0" data-caption="我是一个普通的radio">
                <i class="bh-choice-helper"></i>
                我是一个普通的radio
            </label>
            <label class="bh-radio-label" >
                <input type="radio" name="nl" disabled value="1" data-caption="我是一个不可用的radio，默认状态为未选中">
                <i class="bh-choice-helper"></i>
                我是一个不可用的radio，默认状态为未选中
            </label>
            <label class="bh-radio-label" >
                <input type="radio" name="nl" disabled checked value="1" data-caption="我是一个不可用的radio，默认状态为选中！">
                <i class="bh-choice-helper"></i>
                我是一个不可用的radio，默认状态为选中！
            </label>
        </div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section3" data-show=true data-collapse=true ces-->

```html
<div class="bh-radio bh-radio-group-h">
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
</div>
```

<!--endsec-->

#### radio group 竖直排列

<p>
    <div class="fontsize12">
        <div class="bh-radio bh-radio-group-v">
            <label class="bh-radio-label">
                <input type="radio" name="SHHD_V" value="0" data-caption="我是一个普通的radio">
                <i class="bh-choice-helper"></i>
                我是一个普通的radio
            </label>
        
            <label class="bh-radio-label" >
                <input type="radio" name="SHHD_V" disabled value="1" data-caption="我是一个不可用的radio，默认状态为未选中">
                <i class="bh-choice-helper"></i>
                我是一个不可用的radio，默认状态为未选中
            </label>
        
            <label class="bh-radio-label" >
                <input type="radio" name="SHHD_V" disabled checked value="1" data-caption="我是一个不可用的radio，默认状态为选中！">
                <i class="bh-choice-helper"></i>
                我是一个不可用的radio，默认状态为选中！
            </label>
        </div>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section4" data-show=true data-collapse=true ces-->

```html
<div class="bh-radio bh-radio-group-v">
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
    <label class="bh-radio-label">...</label>
</div>
```

<!--endsec-->


### 多选 - bh-checkbox

#### checkbox 单例 普通、不可用、已选不可用

<p>
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
</p>

<!--sec data-title="代码示例" data-id="section5" data-show=true data-collapse=true ces-->

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

<!--endsec-->

#### checkbox group 水平排列

<p>
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
</p>

<!--sec data-title="代码示例" data-id="section6" data-show=true data-collapse=true ces-->

```html
<div class="bh-checkbox bh-checkbox-group-h">
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
</div>
```

<!--endsec-->

#### checkbox group 竖直排列

<p>
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
</p>

<!--sec data-title="代码示例" data-id="section7" data-show=true data-collapse=true ces-->

```html
<div class="bh-checkbox bh-checkbox-group-v">
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
    <label class="bh-checkbox-label">...</label>
</div>
```

<!--endsec-->


### 开关 - bh-switch

<p>
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
</p>

<!--sec data-title="代码示例" data-id="section8" data-show=true data-collapse=true ces-->

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

<!--endsec-->