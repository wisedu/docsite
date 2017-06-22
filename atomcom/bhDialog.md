# bhDialog - 对话框

## API文档
[http://res.wisedu.com/examples/components-v1/docs/black_hole/module-bhCutStr.html](http://res.wisedu.com/examples/components-v1/docs/black_hole/module-bhCutStr.html)

## 说明
前端对bhDialog封装了三个公共方法，分别是BH_UTILS.bhDialogSuccess，BH_UTILS.bhDialogWarning，BH_UTILS.bhDialogDanger，可以直接使用
```js
BH_UTILS.bhDialogSuccess({
    title:'这是一条提示成功的提醒',
    content:'史蒂夫·乔布斯是一位极具创造力的企业家.',
    callback:function(){
        $("mark").text('按钮的回调函数');
    }
});
```
## 示例

<iframe width="100%" height="500" src="//jsrun.net/c4pKp/embedded/all/light/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>