# 表单样式

### 文本



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
