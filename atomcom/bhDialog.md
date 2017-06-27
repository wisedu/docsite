# bhDialog - 对话框


#### 示例

<iframe width="100%" height="500" src="//jsrun.net/c4pKp/embedded/all/light/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

#### 说明
前端对bhDialog封装了三个公共方法，分别是BH_UTILS.bhDialogSuccess，BH_UTILS.bhDialogWarning，BH_UTILS.bhDialogDanger，可以直接使用

例如：
```js
BH_UTILS.bhDialogSuccess({
    title:'这是一条提示成功的提醒',
    content:'史蒂夫·乔布斯是一位极具创造力的企业家.',
    callback:function(){
        $("mark").text('按钮的回调函数');
    }
});
BH_UTILS.bhDialogWarning({
    title:'这是一条警告信息',
    content:'请确定你所填报的表单已经填写完整，并且无需修改。',
    buttons:[
        {
            text:'真的哦',
            callback:function(){
                $("mark").text("点击了警告框的按钮");
            }
        },
        {
            text:'取消',
            callback:function(){
                $("mark").text("点了取消按钮");
            }
        }
    ]
});
BH_UTILS.bhDialogDanger({
    title:'这是一条危险信息',
    content:'你确认要删除该内容吗？系统将不会保存任何信息，这意味着你不能再找回该内容。你确定吗？',
    callback:function(){
        $("mark").text('删除按钮');
    }
});
```


*****
#### API说明

<iframe width="100%" height="600" src="../bh_apis/1.0/module-bhDialog.html" frameborder="0" id="innerFrame"></iframe>