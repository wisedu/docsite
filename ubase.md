# ubase框架

## 准备工作 {#prepare}

* 安装nodejs环境 -
  [for windows](http://res.wisedu.com/FS/tools/node-v5.6.0-x64.msi) \| - [for mac](http://res.wisedu.com/FS/tools/node-v6.3.0.pkg)
* 设置npm国内镜像，命令行执行:
  `npm config set registry https://registry.npm.taobao.org`
* 安装基础库，命令行执行：
  `npm install -g gulp yo`
* 安装ubase脚手架，命令行执行：
  `npm install -g generator-um`
* 下载 [node\_modules.zip](http://res.wisedu.com/FS/tools/node_modules.zip) 并解压到代码所在盘的根目录
* 下载 [sublime text3](http://res.wisedu.com/FS/tools/sublime text new.zip) 前端编辑器，解压后直接使用，无需安装

## 快速入门 {#quick-start}

* 生成APP目录结构，进入项目待存放目录，打开命令行执行：yo um，选择ubase选项-&gt;输入项目名称-&gt;回车
* 生成APP页面， 进入第一步生成的modules文件夹，打开命令行执行：yo um，选择页面类型-&gt;输入页面名称（名称由字母组成）-&gt; 回答是否纸质弹框页面 -&gt; 回车
* [模板示例页](http://res.wisedu.com/FS/feType)

  * 在config.js中配置modules.  
```js  
    "MODULES": [{

    title: "模块名称",
    route: "modulename"

    }]
```

* 当前目录命令行下执行gulp命令.

* 打开浏览器进入
  [http://localhost:9001](http://localhost:9001/)
  查看.

## 规则约定 {#rule}

### 应用目录结构 {#-}

```
app/
├── modules/
│   ├── modules1/
│   │   ├── modules1.css
│   │   ├── modules1.js
│   │   ├── modules1BS.js
│   │   ├── modules1IndexPage.html
│   │   └── ···
│   ├── modules2/
│   │   ├── modules2.css
│   │   ├── modules2.js
│   │   ├── modules2BS.js
│   │   ├── modules2IndexPage.html
│   │   └── ···
│   └── ···/
├── public/
│   ├── css/
│   │   ├── base.css
│   │   └── style.css
│   └── images/
│       └── ···
├── config.js
└── index.html
```

一个模块至少存在 目录名.js 目录名BS.js 目录名IndexPage.html 三个文件，如需定制样式可以自行添加 目录名.css，模板文件的命名规则：目录名+自定义名称+Page.html

### 事件绑定方式 {#-}

模块中的所有事件处理都通过eventMap来维护，eventMap中key为jquery选择器，value为绑定的事件处理函数，默认绑定的是click事件，如需绑定其他事件，可以在key后@相应的事件. 在事件处理函数中可通过event.currentTarget获取到对应的dom元素

```
eventMap: function() {
    return {
        "#retirementInfoTable .j-row-edit": this.editCb,
        "#advancedQueryPlaceholder@search": this.searchCb,
        ".index-tip@mouseover": this.mouseoverCb
    };
},
```

```
editCb: function(event){
  var wid = $(event.currentTarget).attr('data-x-wid');//通过这种方式可以给事件传递参数
}
```

### 异步数据获取方式 {#-}

目录名BS.js主要负责与后端API交互并进行数据处理, 异步请求使用jquery的Deferred对象做链式处理。

```
getStudentInfo: function(params) {
    var def = $.Deferred();

    utils.doAjax(bs.api.studentInfoUrl, null, 'get').done(function(res) {
        // 这里可以对返回的数据做些处理
        def.resolve(res);
    }).fail(function(res) {
        def.reject(res);
    });

    return def.promise();
}
```

### 路由跳转 {#-}

utils.goto实现路由跳转，第一个参数为跳转后的路由，如果需要在新的tab页打开，则第二个参数置为true

```
utils.goto('module1/detail/1', true);
```

### 页脚位置置底 {#-}

在页面中插入html的时候，如果需要重置页面的页脚位置，可以将html方法的第二个参数置为true

```
this.$rootElement.html(mainView.render(), true);
```

## 路由参数 {#route-params}

路由参数采用restful风格，一般在路由跳转或新开浏览器tab页的时候使用

```
initialize: function() {
    var routeParams = this.getRouterParams();
    var type = routeParams[0];
    var id = routeParams[1];

    switch (type) {
        case 'preview':
            this.initPreviewPage(id);
            break;
        case 'check':
            this.initCheckPage(id);
            break;
        default:
            this.initIndexPage();
    }
},
```

## 子页面 {#sub-page}

纸质弹窗、步骤条中的每个step以及业务上独立的页面需要写入单独的子页面文件夹（包括js,bs,css,html，如果有都要独立），如果子页面中还包含子页面，则在子页面的文件夹中再嵌套其子页面的文件夹。子页面在使用前需要通过pushSubView注册，子页面使用的入口方法为initialize方法, 子页面中有属性parent指向主页面。

## 公共页面 {#common-page}

如果某个子页面在多个模块中都有用到，则需要将其放到public/commonpage/文件夹下，然后在需要使用该子页面的模块中require该子页面即可。

## echarts图表 {#echarts}

统一通过utils.getEcharts\(\)获取echarts对象，然后做后续图表初始化

```
utils.getEcharts().done(function(ec) {
    var myChart = ec.init($obj);//$obj为原生dom对象
    myChart.setOption(option);
});
```

## APP嵌入模式 {#embed}

如果app是通过iframe的方式嵌入的，而且嵌入后希望隐藏APP的header和footer，只显示中间内容区域，则在url中添加min=1参数（注意：该参数需要在\#路由前添加）如：

```
http://res.wisedu.com/FE/HRMS/个人填报单页版/index.html?min=1#/txsbb
```

## 技术选型 {#technology}

* 模块化：requirejs
* 路由：Director
* 模板引擎：Hogan
  [语法参考Mustache](http://blog.csdn.net/p569354158/article/details/8085595)
* 图表：echarts
  [example](http://echarts.baidu.com/examples.html)
* 工具库：lodash
  [API Documentation](https://lodash.com/docs)
* 滚动条美化：jquery.nicescroll
* 组件库：jqxWidgets
  [Documentation](http://www.jqwidgets.com/jquery-widgets-documentation/)



