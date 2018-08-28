# EMAP-MOBILE 初始化文档

## 鸣谢
本组件库完全是自主开发的一个开源共享移动端组件库。感谢各个组件的开发者参与和支持。

---------

## 前置
组件库依赖 bh-mint-ui2、今日校园/微信/钉钉-JSSDK

---------

## 与自己的框架集成

如果要集成此组件库，你必须已经有自己的vue + webpack项目

### 第一步： npm 安装
推荐使用 npm 的方式安装，它能更好地和 [webpack](https://webpack.js.org/) 打包工具配合使用。

```shell
npm install emap-mobile
```

### 第二步：main.js文件中引入

```shell
//import
import emapMobile from 'emap-mobile';
//use
Vue.use(emapMobile);
```
