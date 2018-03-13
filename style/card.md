# 卡片

<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes-1.2.min.css">
<link rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">

<style>
.book-summary{
	font-size:14px;
}
.bhclass,.bhclass section{
	font-size: 12px!important;
	line-height: 20px;
}
.bhclass h3{
	font-size: 16px;line-height: 16px;
	margin: 0;
}
.bh-btn-grouped{
	margin-left: 4px;
	margin-right: 4px;
}
.panel{
    margin-bottom: 72px;
}
</style>

### 基本卡片

<p>
    <div class="bh-clearfix">
    	<div class="bh-card bh-card-lv1 bh-pull-left bh-m-16" style="width:120px;height: 75px">一级卡片</div>
    	<div class="bh-card bh-card-lv2 bh-pull-left bh-m-16" style="width:120px;height: 75px">二级卡片</div>
    	<div class="bh-card bh-card-lv3 bh-pull-left bh-m-16" style="width:120px;height: 75px">三级卡片</div>
    	<div class="bh-card bh-card-lv4 bh-pull-left bh-m-16" style="width:120px;height: 75px">四级卡片</div>
    </div>
</p>

注意：卡片一定需要设置宽度和高度，否则内容超长时，就会将卡片撑开，导致页面不对其

<!--sec data-title="代码示例" data-id="section0" data-show=true data-collapse=true ces-->

```html
<div class="bh-card bh-card-lv1" style="width:120px;height: 75px">一级卡片</div>
<div class="bh-card bh-card-lv2" style="width:120px;height: 75px">二级卡片</div>
<div class="bh-card bh-card-lv3" style="width:120px;height: 75px">三级卡片</div>
<div class="bh-card bh-card-lv4" style="width:120px;height: 75px">四级卡片</div>
```

<!--endsec-->


### 人物卡片

<p>
	<div class="bh-row bh-mv-24 bhclass">
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

选中样式：sc-active

<!--sec data-title="代码示例" data-id="section1" data-show=true data-collapse=true ces-->

```html
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

<!--endsec-->

### 事物卡片

<p>
	<div class="bh-row bh-mv-24 bhclass">
        <!--事物卡片 操作项上滑 正常状态-->
        <div class="sc-panel-thing-1 bh-mh-8">
            <div class="sc-panel-thing-1-image">
                <img src="http://res.wisedu.com/scenes/public/images/demo/user1.png">
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
                <img src="http://res.wisedu.com/scenes/public/images/demo/user2.png">
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

选中样式：sc-active

<!--sec data-title="代码示例" data-id="section2" data-show=true data-collapse=true ces-->

```html

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

<!--endsec-->

### 事物无图片

<p>
	<div class="bh-row bh-mv-24 bhclass">
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

* 选中样式：sc-active
* 默认灰色样式：sc-default

<!--sec data-title="代码示例" data-id="section3" data-show=true data-collapse=true ces-->

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

<!--endsec-->

### 对角线卡片

<p>
	<div class="bh-row bh-mv-24 bh-clearfix">
	    <div class="bh-card bh-card-lv1 bh-pull-left bh-m-8" style="width: 272px;">
	        <div class="sc-panel-diagonalStrips sc-panel-warning">
	            <div class="sc-panel-diagonalStrips-bar">待审核</div>
	            <div class="sc-panel-diagonalStrips-text">生源核对</div>
	        </div>
	    </div>
    	<div class="bh-card bh-card-lv1 bh-pull-left bh-m-8" style="width: 272px;">
	        <div class="sc-panel-diagonalStrips sc-panel-success">
	            <div class="sc-panel-diagonalStrips-bar">已完成</div>
	            <div class="sc-panel-diagonalStrips-text">推荐表</div>
	        </div>
	    </div>
    	<div class="bh-card bh-card-lv1 bh-pull-left bh-m-8" style="width: 272px;">
	        <div class="sc-panel-diagonalStrips">
	            <div class="sc-panel-diagonalStrips-bar">未填写</div>
	            <div class="sc-panel-diagonalStrips-text">就业意向登记</div>
	        </div>
	    </div>
	</div>
</p>

<!--sec data-title="代码示例" data-id="section4" data-show=true data-collapse=true ces-->

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

<!--endsec-->

### 提示信息卡片

<p>
	<div class="sc-panel-list bh-card bh-card-lv1 bhclass">
        <div class="sc-panel-list-header">
            <h3>校园活动</h3>
            <div class="sc-panel-list-caption">更多<i class="iconfont icon-keyboardarrowright"></i></div>
        </div>
        <section class="sc-panel-list-section sc-panel-list-prompt">
            <div>
                <img src="http://res.wisedu.com/fe_components/images/errorTip/unable_to_use_the_service.png">
                <div class="bh-color-grey-3">最近没有任何校园活动</div>
            </div>
        </section>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section5" data-show=true data-collapse=true ces-->

```html
<div class="sc-panel-list bh-card bh-card-lv1">
    <div class="sc-panel-list-header">
        <h3>校园活动</h3>
        <div class="sc-panel-list-caption">更多<i class="iconfont icon-keyboardarrowright"></i></div>
    </div>
    <section class="sc-panel-list-section sc-panel-list-prompt">
        <div>
            <img src="http://res.wisedu.com/fe_components/images/errorTip/unable_to_use_the_service.png">
            <div class="bh-color-grey-3">最近没有任何校园活动</div>
        </div>
    </section>
</div>
```

<!--endsec-->

<p>
	<div class="sc-panel-list bh-card bh-card-lv1 bhclass">
        <div class="sc-panel-list-header">
            <h3>校园活动</h3>
            <div class="sc-panel-list-caption">更多<i class="iconfont icon-keyboardarrowright"></i></div>
        </div>
        <section class="sc-panel-list-section bh-pv-8 bh-ph-16">
            <div class="sc-panel-list-section-left">
                <h3 class="bh-str-cut">个人年度计划总结PPT汇报演示个人年度计划总结PPT汇报演示</h3>
                <div class="bh-color-grey-3">10月1日</div>
            </div>
            <img class="sc-panel-list-section-right" src="http://res.wisedu.com/fe_components/images/errorTip/unable_to_use_the_service.png">
        </section>
        <section class="sc-panel-list-section bh-pv-8 bh-ph-16">
            <div class="sc-panel-list-section-left">
                <h3 class="bh-str-cut">个人年度计划总结PPT汇报演示个人年度计划总结PPT汇报演示</h3>
                <div class="bh-color-grey-3">10月1日</div>
            </div>
            <img class="sc-panel-list-section-right" src="http://res.wisedu.com/fe_components/images/errorTip/unable_to_use_the_service.png">
        </section>
    </div>
</p>

<!--sec data-title="代码示例" data-id="section6" data-show=true data-collapse=true ces-->

```html
<div class="sc-panel-list bh-card bh-card-lv1">
    <div class="sc-panel-list-header">
        <h3>校园活动</h3>
        <div class="sc-panel-list-caption">更多<i class="iconfont icon-keyboardarrowright"></i></div>
    </div>
    <section class="sc-panel-list-section bh-pv-8 bh-ph-16">
        <div class="sc-panel-list-section-left">
            <h3 class="bh-str-cut">个人年度计划总结PPT汇报演示个人年度计划总结PPT汇报演示</h3>
            <div class="bh-color-grey-3">10月1日</div>
        </div>
        <img class="sc-panel-list-section-right" src="http://res.wisedu.com/fe_components/images/errorTip/unable_to_use_the_service.png">
    </section>
    <section class="sc-panel-list-section bh-pv-8 bh-ph-16">
        <div class="sc-panel-list-section-left">
            <h3 class="bh-str-cut">个人年度计划总结PPT汇报演示个人年度计划总结PPT汇报演示</h3>
            <div class="bh-color-grey-3">10月1日</div>
        </div>
        <img class="sc-panel-list-section-right" src="http://res.wisedu.com/fe_components/images/errorTip/unable_to_use_the_service.png">
    </section>
</div>
```

<!--endsec-->