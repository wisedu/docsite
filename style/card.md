# 卡片

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">

<style>
.book-summary{
	font-size:14px;
}
.fontsize12{
	font-size: 12px!important;
}
.bh-btn-grouped{
	margin-left: 4px;
	margin-right: 4px;
}

</style>

### 基本卡片

<div class="bh-clearfix">
	<div class="bh-card bh-card-lv1 bh-pull-left bh-m-16" style="width:120px;height: 75px">一级卡片</div>
	<div class="bh-card bh-card-lv2 bh-pull-left bh-m-16" style="width:120px;height: 75px">二级卡片</div>
	<div class="bh-card bh-card-lv3 bh-pull-left bh-m-16" style="width:120px;height: 75px">三级卡片</div>
	<div class="bh-card bh-card-lv4 bh-pull-left bh-m-16" style="width:120px;height: 75px">四级卡片</div>
</div>

```html
<div class="bh-card bh-card-lv1" style="width:120px;height: 75px">一级卡片</div>
<div class="bh-card bh-card-lv2" style="width:120px;height: 75px">二级卡片</div>
<div class="bh-card bh-card-lv3" style="width:120px;height: 75px">三级卡片</div>
<div class="bh-card bh-card-lv4" style="width:120px;height: 75px">四级卡片</div>
卡片需要设置宽度和高度
```

### 人物卡片

<p>
	<div class="bh-row bh-mv-24 fontsize12">
	    <div class="sc-panel-user-1 bh-mh-8">
	        <div class="sc-panel-user-1-image">
	            <img src="http://res.wisedu.com/scenes/public/images/demo/userPanel.jpg">
	        </div>
	        <div class="sc-panel-user-1-container bh-animate-all bh-animate-fast">
	            <div class="sc-panel-user-1-description">
	                <div class="sc-panel-user-1-header">
	                    <div class="sc-panel-user-1-title">朱小如</div>
	                    <div class="sc-panel-user-1-info">00021323 女 21岁</div>
	                </div>
	                <div class="sc-panel-user-1-category bh-mb-8">教育与心理学院  研究生</div>
	                <div class="sc-panel-user-1-content">朱小如毕业于南京市第五中学，2012年考入南京艺术学院，传媒学院，数字媒体</div>
	            </div>

	            <div class="sc-panel-user-1-operate bh-animate-bottom bh-animate-fast">
	                <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">接入管理</span> | <span class="bh-mh-4">查看详情</span>
	            </div>
	        </div>
	    </div>
	    <div class="sc-panel-user-1 sc-active bh-mh-8">
	        <div class="sc-panel-user-1-image">
	            <img src="http://res.wisedu.com/scenes/public/images/demo/userPanel.jpg">
	        </div>
	        <div class="sc-panel-user-1-container bh-animate-all bh-animate-fast">
	            <div class="sc-panel-user-1-description">
	                <div class="sc-panel-user-1-header">
	                    <div class="sc-panel-user-1-title">朱小如</div>
	                    <div class="sc-panel-user-1-info">00021323 女 21岁</div>
	                </div>
	                <div class="sc-panel-user-1-category bh-mb-8">教育与心理学院  研究生</div>
	                <div class="sc-panel-user-1-content">朱小如毕业于南京市第五中学，2012年考入南京艺术学院，传媒学院，数字媒体</div>
	            </div>

	            <div class="sc-panel-user-1-operate bh-animate-bottom bh-animate-fast">
	                <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">接入管理</span> | <span class="bh-mh-4">查看详情</span>
	            </div>
	        </div>
	    </div>
	</div>
</p>

```html
选中样式：sc-active
<div class="sc-panel-user-1 bh-mh-8 sc-active">
    <!--左边照片-->
    <div class="sc-panel-user-1-image">
        <img src="http://res.wisedu.com/scenes/public/images/demo/userPanel.jpg">
    </div>
    <!--中间内容-->
    <div class="sc-panel-user-1-container bh-animate-all bh-animate-fast">
        <div class="sc-panel-user-1-description">
        	<!--标题-->
            <div class="sc-panel-user-1-header">
                <div class="sc-panel-user-1-title">朱小如</div>
                <div class="sc-panel-user-1-info">00021323 女 21岁</div>
            </div>
            <!--内容-->
            <div class="sc-panel-user-1-category bh-mb-8">教育与心理学院  研究生</div>
            <div class="sc-panel-user-1-content">朱小如毕业于南京市第五中学，2012年考入南京艺术学院，传媒学院，数字媒体</div>
        </div>
        <!--下侧菜单-->
        <div class="sc-panel-user-1-operate bh-animate-bottom bh-animate-fast">
            <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">接入管理</span> | <span class="bh-mh-4">查看详情</span>
        </div>
    </div>
</div>
```

### 事物卡片

<p>
	<div class="bh-row bh-mv-24 fontsize12">
        <!--事物卡片 操作项上滑 正常状态-->
        <div class="sc-panel-thing-1 bh-mh-8">
            <div class="sc-panel-thing-1-image">
                <img src="http://res.wisedu.com/scenes/public/images/demo/userPanel.jpg">
            </div>
            <div class="sc-panel-thing-1-container bh-animate-all bh-animate-fast">
                <div class="sc-panel-thing-1-description">
                    <div class="sc-panel-thing-1-header">
                        <div class="sc-panel-thing-1-title">朱小如</div>
                    </div>
                    <div class="sc-panel-thing-1-subject">
                        <div class="sc-panel-thing-1-subjectKey sc-width-50">座位数</div>
                        <div class="sc-panel-thing-1-subjectValue">1280</div>
                    </div>
                    <div class="sc-panel-thing-1-subject">
                        <div class="sc-panel-thing-1-subjectKey sc-width-50">价格</div>
                        <div class="sc-panel-thing-1-subjectValue">210元/场</div>
                    </div>
                </div>

                <div class="sc-panel-thing-1-operate bh-animate-bottom bh-animate-fast">
                    <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
                </div>
            </div>
        </div>

        <!--事物卡片 操作项上滑 正常状态-->
        <div class="sc-panel-thing-1 sc-active bh-mh-8">
            <div class="sc-panel-thing-1-image">
                <img src="http://res.wisedu.com/scenes/public/images/demo/userPanel.jpg">
            </div>
            <div class="sc-panel-thing-1-container bh-animate-all bh-animate-fast">
                <div class="sc-panel-thing-1-description">
                    <div class="sc-panel-thing-1-header">
                        <div class="sc-panel-thing-1-title">朱小如</div>
                    </div>
                    <div class="sc-panel-thing-1-subject">
                        <div class="sc-panel-thing-1-subjectKey sc-width-50">座位数</div>
                        <div class="sc-panel-thing-1-subjectValue">1280</div>
                    </div>
                    <div class="sc-panel-thing-1-subject">
                        <div class="sc-panel-thing-1-subjectKey sc-width-50">价格</div>
                        <div class="sc-panel-thing-1-subjectValue">210元/场</div>
                    </div>
                </div>

                <div class="sc-panel-thing-1-operate bh-animate-bottom bh-animate-fast">
                    <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
                </div>
            </div>
        </div>
    </div>
</p>

```html
选中样式：sc-active
<div class="sc-panel-thing-1 bh-mh-8 sc-active">
	<!--左边照片-->
    <div class="sc-panel-thing-1-image">
        <img src="http://res.wisedu.com/scenes/public/images/demo/userPanel.jpg">
    </div>
    <!--中间内容-->
    <div class="sc-panel-thing-1-container bh-animate-all bh-animate-fast">
        <div class="sc-panel-thing-1-description">
        	<!--标题-->
            <div class="sc-panel-thing-1-header">
                <div class="sc-panel-thing-1-title">朱小如</div>
            </div>
            <!--内容-->
            <div class="sc-panel-thing-1-subject">
                <div class="sc-panel-thing-1-subjectKey sc-width-50">座位数</div>
                <div class="sc-panel-thing-1-subjectValue">1280</div>
            </div>
            <div class="sc-panel-thing-1-subject">
                <div class="sc-panel-thing-1-subjectKey sc-width-50">价格</div>
                <div class="sc-panel-thing-1-subjectValue">210元/场</div>
            </div>
        </div>
        <!--下侧菜单-->
        <div class="sc-panel-thing-1-operate bh-animate-bottom bh-animate-fast">
            <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
        </div>
    </div>
</div>
```

### 事物无图片

<p>
	<div class="bh-row bh-mv-24 fontsize12">
        <!--事物卡片无图 操作项上滑 正常状态-->
        <div class="sc-panel-thingNoImg-1 bh-mh-8">
            <div class="sc-panel-thingNoImg-1-container bh-animate-all bh-animate-fast">
                <div class="sc-panel-thingNoImg-1-description">
                    <div class="sc-panel-thingNoImg-1-header">
                        <div class="sc-panel-thingNoImg-1-title">朱小如</div>
                    </div>
                    <div class="sc-panel-thingNoImg-1-subject">
                        <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">座位数</div>
                        <div class="sc-panel-thingNoImg-1-subjectValue">1280</div>
                    </div>
                    <div class="sc-panel-thingNoImg-1-subject">
                        <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">价格</div>
                        <div class="sc-panel-thingNoImg-1-subjectValue">210元/场</div>
                    </div>
                </div>

                <div class="sc-panel-thingNoImg-1-operate bh-animate-bottom bh-animate-fast">
                    <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
                </div>
            </div>
        </div>

        <div class="sc-panel-thingNoImg-1 sc-active bh-mh-8">
            <div class="sc-panel-thingNoImg-1-container bh-animate-all bh-animate-fast">
                <div class="sc-panel-thingNoImg-1-description">
                    <div class="sc-panel-thingNoImg-1-header">
                        <div class="sc-panel-thingNoImg-1-title">朱小如</div>
                    </div>
                    <div class="sc-panel-thingNoImg-1-subject">
                        <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">座位数</div>
                        <div class="sc-panel-thingNoImg-1-subjectValue">1280</div>
                    </div>
                    <div class="sc-panel-thingNoImg-1-subject">
                        <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">价格</div>
                        <div class="sc-panel-thingNoImg-1-subjectValue">210元/场</div>
                    </div>
                </div>

                <div class="sc-panel-thingNoImg-1-operate bh-animate-bottom bh-animate-fast">
                    <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
                </div>
            </div>
        </div>

        <div class="sc-panel-thingNoImg-1 sc-active sc-default bh-mh-8">
            <div class="sc-panel-thingNoImg-1-container bh-animate-all bh-animate-fast">
                <div class="sc-panel-thingNoImg-1-description">
                    <div class="sc-panel-thingNoImg-1-header">
                        <div class="sc-panel-thingNoImg-1-title">朱小如</div>
                    </div>
                    <div class="sc-panel-thingNoImg-1-subject">
                        <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">座位数</div>
                        <div class="sc-panel-thingNoImg-1-subjectValue">1280</div>
                    </div>
                    <div class="sc-panel-thingNoImg-1-subject">
                        <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">价格</div>
                        <div class="sc-panel-thingNoImg-1-subjectValue">210元/场</div>
                    </div>
                </div>

                <div class="sc-panel-thingNoImg-1-operate bh-animate-bottom bh-animate-fast">
                    <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
                </div>
            </div>
        </div>
    </div>
</p>

```html
<div class="sc-panel-thingNoImg-1 sc-active sc-default bh-mh-8">
    <div class="sc-panel-thingNoImg-1-container bh-animate-all bh-animate-fast">
        <!--中间内容-->
        <div class="sc-panel-thingNoImg-1-description">
        	<!--标题-->
            <div class="sc-panel-thingNoImg-1-header">
                <div class="sc-panel-thingNoImg-1-title">朱小如</div>
            </div>
            <!--内容-->
            <div class="sc-panel-thingNoImg-1-subject">
                <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">座位数</div>
                <div class="sc-panel-thingNoImg-1-subjectValue">1280</div>
            </div>
            <div class="sc-panel-thingNoImg-1-subject">
                <div class="sc-panel-thingNoImg-1-subjectKey sc-width-50">价格</div>
                <div class="sc-panel-thingNoImg-1-subjectValue">210元/场</div>
            </div>
        </div>
        <!--下侧菜单-->
        <div class="sc-panel-thingNoImg-1-operate bh-animate-bottom bh-animate-fast">
            <span class="bh-mh-4">编辑</span> | <span class="bh-mh-4">查看详情</span>
        </div>
    </div>
</div>
```

### 对角线卡片

<p>
	<div class="bh-row bh-mv-24">
	    <div class="bh-card bh-card-lv1" style="width: 272px;">
	        <div class="sc-panel-diagonalStrips sc-panel-warning">
	            <div class="sc-panel-diagonalStrips-bar">待审核</div>
	            <div class="sc-panel-diagonalStrips-text">生源核对</div>
	        </div>
	    </div>
    	<div class="bh-card bh-card-lv1" style="width: 272px;">
	        <div class="sc-panel-diagonalStrips sc-panel-success">
	            <div class="sc-panel-diagonalStrips-bar">已完成</div>
	            <div class="sc-panel-diagonalStrips-text">推荐表</div>
	        </div>
	    </div>
    	<div class="bh-card bh-card-lv1" style="width: 272px;">
	        <div class="sc-panel-diagonalStrips">
	            <div class="sc-panel-diagonalStrips-bar">未填写</div>
	            <div class="sc-panel-diagonalStrips-text">就业意向登记</div>
	        </div>
	    </div>
	</div>
</p>

```html
    <div class="bh-card bh-card-lv1" style="width: 272px;">
        <div class="sc-panel-diagonalStrips sc-panel-warning">
            <div class="sc-panel-diagonalStrips-bar">待审核</div>
            <div class="sc-panel-diagonalStrips-text">生源核对</div>
        </div>
    </div>
    <div class="bh-card bh-card-lv1" style="width: 272px;">
        <div class="sc-panel-diagonalStrips sc-panel-success">
            <div class="sc-panel-diagonalStrips-bar">已完成</div>
            <div class="sc-panel-diagonalStrips-text">推荐表</div>
        </div>
    </div>
    <div class="bh-card bh-card-lv1" style="width: 272px;">
        <div class="sc-panel-diagonalStrips">
            <div class="sc-panel-diagonalStrips-bar">未填写</div>
            <div class="sc-panel-diagonalStrips-text">就业意向登记</div>
        </div>
    </div>
```