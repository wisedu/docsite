# BH Mint UI 2 使用文档

## 鸣谢
本组件库是基于 MintUI 更换部分 Vant 组件，加上自有开发的组件形成的移动组件库。

感谢开源对大家的贡献，我们的组件库代码地址： [bh-mint-ui2](https://github.com/wisedu/bh-mint-ui2)


---------

## 阅读者请注意
当前这一页的内容是介绍组件与框架集成，左侧导航有对每个组件说明的API文档
> * 你是 **金智教育移动框架** 使用者，[请点击这里](http://res.wisedu.com/FS/docsite/mobile/mobile.html) 可以更好的了解如何集成使用
> * 如果你 **已有项目并且很有经验**，要与自己的框架做集成，可以继续浏览以下内容

---------

## 与自己的框架集成
**非金智教育移动框架**

如果要运行以下的例子，你必须已经有自己的vue项目

### 方式1：npm 安装
推荐使用 npm 的方式安装，它能更好地和 [webpack](https://webpack.js.org/) 打包工具配合使用。

```shell
npm i bh-mint-ui2 -S
```

### 方式2：CDN 集成到现有的首页

可以通过 [Vue全家桶](https://res.wisedu.com/bower_components/vue2) / [BH-MINT-UI2](https://res.wisedu.com/fe_components/mobile/MINT/) 获取到最新版本的资源，在页面上引入 js 和 css 文件即可开始使用。

```html
<!-- 引入样式 (注：换肤文件`skin.css`置于style.min.css之前)-->
<link rel="stylesheet" href="https://res.wisedu.com/fe_components/skins/mint2.0/skin.css">
<link rel="stylesheet" href="https://res.wisedu.com/fe_components/mobile/MINT/cpdaily/style.min.css">
<link rel="stylesheet" href="https://res.wisedu.com/bh_components/mobile/1.0.0/bh-lib.min.css">
<!-- 引入组件库 -->
<script src="https://res.wisedu.com/bower_components/vue2/vue.min.js"></script>
<script src="https://res.wisedu.com/fe_components/mobile/MINT/index.js"></script>
```


### 方式3：全新的页面中引用
通过 CDN 的方式我们可以很容易地使用 BH Mint UI 2 写出一个 Hello world 页面。


```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <!-- 引入样式 -->
  <link rel="stylesheet" href="https://res.wisedu.com/fe_components/skins/mint2.0/skin.css">
  <link rel="stylesheet" href="https://res.wisedu.com/fe_components/mobile/MINT/style.min.css">
</head>
<body>
  <div id="app">
    <mt-button @click.native="handleClick">按钮</mt-button>
  </div>
</body>
  <!-- 先引入 Vue -->
  <script src="https://res.wisedu.com/bower_components/vue2/vue.min.js"></script>
  <!-- 引入组件库 -->
  <script src="https://res.wisedu.com/fe_components/mobile/MINT/index.js"></script>
  <script>
    new Vue({
      el: '#app',
      methods: {
        handleClick: function() {
          window.Vue.$toast('Hello world!')
        }
      }
    })
  </script>
</html>
```



如果是通过 npm 安装，并希望配合 webpack 使用，请继续阅读。

<br>

**关于事件绑定**

在 Vue 2.0 中，为自定义组件绑定原生事件必须使用 `.native` 修饰符：
<!-- ::: demo -->
```html
<my-component @click.native="handleClick">Click Me</my-component>
```
<!-- ::: -->
从易用性的角度出发，我们对 `Button` 组件进行了处理，使它可以监听 `click` 事件：
<!-- ::: demo -->
```html
<mt-button @click="handleButtonClick">Click Me</mt-button>
```
<!-- ::: -->
但是对于其他组件，还是需要添加 `.native` 修饰符。

<script>
  import { Toast } from 'bh-mint-ui2';
  export default {
    methods:{
      handleClick:function() {
        Toast('Hello world!')
      },
      handleButtonClick:function(){
      }
    }
  };
</script>


## 想从零开始用 Webpack 构建项目
**非金智教育移动框架**

### 使用 vue-cli

```bash
npm install -g vue-cli

vue init webpack projectname
```

### 引入 BH Mint UI 2

你可以引入整个 BH Mint UI 2，或是根据需要仅引入部分组件。我们先介绍如何引入完整的 BH Mint UI 2。

#### 完整引入

在 main.js 中写入以下内容：
```javascript
import Vue from 'vue'
import MintUI from 'bh-mint-ui2'
import 'mint-ui/lib/style.css'
import App from './App.vue'

Vue.use(MintUI)

new Vue({
  el: '#app',
  components: { App }
})
```
以上代码便完成了 BH Mint UI 2 的引入。需要注意的是，样式文件需要单独引入。

#### 按需引入

借助 [babel-plugin-component](https://github.com/QingWei-Li/babel-plugin-component)，我们可以只引入需要的组件，以达到减小项目体积的目的。

首先，安装 babel-plugin-component：

```bash
npm install babel-plugin-component -D
```

然后，将 .babelrc 修改为：
```json
{
  "presets": [
    ["es2015", { "modules": false }]
  ],
  "plugins": [["component", [
    {
      "libraryName": "bh-mint-ui2",
      "style": true
    }
  ]]]
}
```

如果你只希望引入部分组件，比如 Button 和 Cell，那么需要在 main.js 中写入以下内容：

```javascript
import Vue from 'vue'
import { Button, Cell } from 'bh-mint-ui2'
import App from './App.vue'

Vue.component(Button.name, Button)
Vue.component(Cell.name, Cell)
/* 或写为
 * Vue.use(Button)
 * Vue.use(Cell)
 */

new Vue({
  el: '#app',
  components: { App }
})
```

### 开始使用

至此，一个基于 Vue 和 Mint UI 的开发环境已经搭建完毕，现在就可以编写代码了。启动开发模式：

```bash
npm run dev
```

编译：

```bash
npm run build
```
各个组件的使用方法请参阅它们各自的文档。
