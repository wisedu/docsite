# 移动框架与组件

说明: 本文档用于指导前端 H5 App 的开发，如需开发其他其他功能组件比如小卡片等，不适用本文档

## 前期准备
* Vue 的基本概念[vue文档](https://cn.vuejs.org/)
* es6 开发基本知识 [es6 基本文档](http://es6.ruanyifeng.com/)
* 移动门户[App](https://www.pgyer.com/VGkN)
* 示例代码 <a href="assets/newOnlineConsultation.zip" target="_blank">newOnlineConsultation.zip</a>

## 1、搭建脚手架

### 1.1、安装node环境
Node 环境(Node >=4.0.0, npm >= 3.0.0)[下载地址](https://nodejs.org/zh-cn/)<br>
打开命令行界面，首先检查有没有安装 npm 命令 检查方法
```
node -v
```
```
npm -v
```
出现版本号即为安装成功（如下图所示）。

![](/assets/Snip20170320_40.png)<br>
注：执行命令可将npm指向淘宝镜像以提升安装速度(npm -> cnpm)
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
### 1.2、安装脚手架工具


通过 npm 安装 vue 脚手架命令行工具

```
npm i -g vue-cli --registry=https://registry.npm.taobao.org
(或：cnpm i -g vue-cli)
```

退出命令行，重新进入，检查有没有安装成功
```
vue --version

```

![](/assets/Snip20170320_41.png)

如果没有正确弹出版本号，请尝试用管理员身份启动命令行

### 1.3、初始化脚手架

```
vue init wisedu/bh-vue2-mobile yourProject

```
命令会在当前的文件夹下生成一个文件夹，这个文件夹就是我们的项目文件夹。  
![](/assets/Snip20170320_42.png)  
此时填写的配置项，等脚手架下载下来之后，都可在package.json文件中修改。  
最后一步的 use native SDK（是否在脚手架中引入SDK） 除外。    

## 2、 运行项目

1.进入上一步创建的文件夹，运行命令(初次运行此项目时需要输入)

```
npm install
```
命令运行后，会去下载相关的依赖<br>
2.然后启动项目

```
npm run dev

```
项目启动在8080端口上，如果希望项目启动在，其他端口上，请修改 webpack.config.js的 port

![](/assets/Snip20170320_39.png)

可以通过chrome 开发者工具，模拟出手机的屏幕方便开发

## 3、项目基本结构

### 3.1、目录说明

```
my-project
├── doc //放置项目的文档，包括后端文档，设计文档等，方便多人开发这个项目的时候共享文档
├── src //项目源代码，开发人员编写的源代码都在这个目录下
│   └── components //页面级别的公用组件, 例如在某个项目里共同使用的用户信息展示, 某些共用的复杂弹窗等等
│   └── pages //业务模块文件夹, 按照业务逻辑区分的业务模块文件夹
│   └── vuex //用于放置 vuex 相关的文件(mutation, store, action, getter)
│   └── App.vue
│   └── api.js //接口地址
│   └── main.js //入口
│   └── router.js //路由
│   └── style.css //一些全局样式
│   └── utils.js //保存项目公共方法
├── build
│   └── deploy.js //打包脚本
├── static //一些样式，和计算root fontsize 的文件
│   └── assets //图片资源
│   └── css //css资源
│   └── js //js资源
├── .babelrc //babel配置
├── .gitignore
├── README.md
├── index.html
├── package.json
├── webpack.config.js
```
### 3.2、目录规范

* pages 目录下有一个业务建一个子文件夹, 文件夹以驼峰命名, 业务的主入口文件与文件夹名相同(避免 sourceMap 无法区别文件问题), 其他文件也以驼峰命名
* components 目录下也分别建子文件夹, 文件夹以驼峰命名, 业务的主入口文件与文件夹名相同(避免 sourceMap 无法区别文件问题), 其他文件也以驼峰命名
* vuex 目录下的命名规范见下文
vuex 命名规范
vuex 涉及的概念比较多 (mutation, store, action, getter), 文件和文件夹命名依旧驼峰
 * store.js 用于暴露最终的 store 对象
 * action.js 用于集合所有的 action
 * mutation 和 store 为了防止出现歧义, 原则上都必须分模块, 即使页面只有一个 vuex 的模块, 也需要在 vuex/module
目录下建立一个独立的文件存放 相应的 mutation 和 store

## 4、组件相关

向 mintUI 致敬

基于 mintUI 2.0的基础上 做了主题和组件的扩展

### 4.1、 组件引入方法

在需要使用组件的*.vue页面，通过 ES6 的 import 语法，引入组件，并在 component 区域注册需要用到的组件<br>
具体的使用方法，可以参考附件中的示例代码，原理请参考vue官网 https://cn.vuejs.org

```html
  <template>
    <div>
      <mt-cell title="标题文字" to="//github.com" is-link value="带链接"></mt-cell>
      <mt-button type='primary' size='large' @click="sumbit">提交</mt-button>
      <mt-field label="密码" placeholder="请输入密码" type="password"></mt-field>
    </div>
</template>
<style scoped>
    div{
      font-size: 20px;
      background: #fff;
    }
</style>
<script>
    import utils from '../../utils'
    import api from '../../api';
    import {
        Toast,
        Indicator,
        Cell,
        Button, 
        Field
    } from 'bh-mint-ui2';
    export default {
        components: {
            [Cell.name]: Cell,            
            [Button.name]: Button,
            [Field.name]: Field
        },
        data() {
            return {
                num: 1,
                str: 'hello world'
            }
        },
        mounted() {
            SDK.setTitleText('我是标题');          
            this.load();            
        },
        methods: {
            load() {

            }
        }
    }
</script>
```

### 4.2、组件使用方法

* 项目站点 https://github.com/wisedu/bh-mint-ui2
* 文档地址 https://wisedu.github.io/bh-mint-ui2-doc/#!/zh-cn2

### 4.3、字体图标使用方法
* 移动字体图标库(https://res.wisedu.com/fe_components/iconfont_mobile/demo_fontclass.html)

字体图标的cdn引入方式（已在脚手架中配置）
```html
<link rel="stylesheet" href="https://res.wisedu.com/fe_components/iconfont_mobile/iconfont.css">
```

手机查看请扫码

![](/assets/1489992182.png)

## 5、Hybrid SDK 相关 

### 5.1、介绍

Hybrid SDK 是前端应用调用客户端原生能力的桥梁，是对原生能力的封装，比如你想调起原生的图片浏览器，新开一个 webview 页面，设置原生的头，隐藏原生的头等，都会涉及到 Hybrid SDK

### 5.2、SDK 引入方法

在脚手架中已经集成了今日校园和部分微信的SDK，项目在实际移动环境中初始化成功之后会自动创建一个全局变量SDK，所以在组件内可直接通过SDK这个变量直接调用控制原生功能的方法即可。<br>
例：设置标题头
```
SDK.setTitleText('我是标题')
```
获取今日校园登录信息
```
SDK.bh.cpdaily.getUserInfo( function(info){
    console.log(info);
});
```

### 5.3、SDK 文档

如果想了解具体有哪些 SDK 可以调用，需要的参数，可查看详细API。[ SDK 文档](http://static.cpdaily.com/jssdk/index.html)

## 6、代码调试

请开发 App 的负责人和后端沟通解决跨域的问题，否则调试只能在 pc 浏览器的 chrome 下进行，其他真机或者手机浏览器调试都不行

### 6.1、pc 浏览器调试

chrome 打开开发者工具，点击模拟手机，即可调试应用

![](/assets/Snip20170320_43.png)

如果服务端不支持跨域，需要打开浏览器时禁掉跨域

mac: 

```
open -n /Applications/Google\ Chrome.app/ --args --disable-web-security  --user-data-dir=/Users/a123/Documents/MyChromeDevUserData 
```
注：上述的'/Users/a123/Documents/MyChromeDevUserData'是在本地'文稿'下建的一个空目录<br>
windows:

```
http://www.cnblogs.com/laden666666/p/5544572.html
```
需要先完全退出浏览器再重新打开才能生效

### 6.2、手机浏览器

直接使用手机浏览器访问，本机 ip:端口，然后Android 可以借助远程 debug 工具调试手机网页[debug](http://wiki.jikexueyuan.com/project/chrome-devtools/remote-debugging-on-android.html)<br>
ios 可以利用 safari 进行调试
1. 在iOS设备上打开允许调试:设置→Safari→高级→打开”web检查器“
2. 在MAC上打开Safari的开发菜单:顶部菜单栏“Safari”→偏好设置→高级→打开”在菜单栏中显示“开发”菜单
3. 在iOS设备上的Safari浏览器中打开要调试的页面，然后切换到MAC的Safari，在顶部菜单栏选择“开发”→找到你的iOS设备名称→右边
二级菜单选择需要调试的对应标签页，即可开始远程调试
4. 如果没有iOS设备，也可以在Xcode中模拟一台，点击顶部“Xcode”→“Open Developer Tool”→“iOS
Simulator”即可打开一个iOS设备的模拟器，并且模拟器里面Safari打开的页面，也是能通过上个步骤中MAC上的Safari调试。


### 6.3、应用内真机调试

#### 需要的材料（今日校园为例）：

1. 手机上装有测试版今日校园，[下载地址](http://www.pgyer.com/cpdaily)
2. 今日校园的服务里有一个自己的可以打开的应用
3. 电脑上装有抓包调试工具spy-debugger(https://github.com/wuchangming/spy-debugger)    
注：spy-debugger不可用cnpm安装
#### 调试的步骤：

1. 打开手机连上无线，设置 -> 无线网络 ->http代理 改为手动，设置服务器地址为开发的电脑的IP，端口号设为9888
2. 打开电脑的命令行窗口，执行 spy-debugger 命令启动调试服务器（自动在浏览器打开一个窗口）
3. 打开今日校园点进自己的应用即可开始页面调试或者请求抓包  
注：利用spy-debugger,其他类型的调试类似（spy-debugger不可用cnpm安装）
## 7、打包上线

#### 目的：
1. 通过手机访问今日校园客户端 -> 服务 找到你发布的应用，进行功能自测
2. 应用开发 -> 应用测试 -> 应用上线（发布到现场）
### 7.1、老版本campusphere平台新建应用流程

1. 登录 [campusphere开发者中心](http://www.campusphere.cn/appcenter)
2. 注册新应用的信息，具体内容见下图
![](/assets/campusphere1.png)
![](/assets/campusphere2.png)
![](/assets/campusphere3.png)
新建成功之后产生应用ID，编辑当前版本，配置授权地址
![](/assets/campusphere4.png)
* 创建新版本，命名要求：swm + 应用名称的拼音缩写 + app，如：swmlxapp = 移动离校(swm代表学工移动，其他业务线可使用自己的规则)
* 授权地址配置：/sys/funauthapp/qxgl.do?appName=ydyysl&appId=5082200864155944&min=1
3. 获取开发文件 app_info.xml（必须） 放入项目脚手架根目录，如果需要 permission.xml（非必须）文件则询问相关人员拿到，也放入根目录。通过源代码打包，打包命令：npm run deploy。这个命令会在项目目录下生成一个 zip 包，zip 包的名字就是在初始化项目脚手架的时候询问的名字（可在package.json文件中修改相关信息）。
4. 在刚才新建的应用，点击 进入开发环境 -> 应用包管理 -> 上传安装包 -> 接入管理 接入到测试环境，并通知测试部署授权上线
5. 测试部署成功之后可在今日校园客户端中打开。 amptest测试租户即是学工测试环境

## 特别注意

**待应用通过测试确认没有问题之后，才可点击'发布到运行环境'。不要轻易发布**
### 7.2、新版本campusphere平台新建应用流程(此处以特例公共服务应用为例) 

1. 登录 [campusphere_2.2开发者中心](http://www.campusphere.cn/appcenter_2.2/index.html)
2. 注册新应用的信息，具体内容见下图
![](/assets/ampusphere_2.2_1.png)
![](/assets/ampusphere_2.2_2.png)
![](/assets/ampusphere_2.2_3.png)
![](/assets/ampusphere_2.2_4.png)
* 创建新版本，命名要求：pubm + 应用名称的拼音缩写 + app，如：pubmcjcxapp = 移动成绩查询(pubm代表公共服务移动，其他业务线可使用自己的规则)
* 授权地址配置：/sys/pubmcjcxapp/auth.do?min=1
3. 获取开发文件 app_info.xml（必须） 放入项目脚手架根目录，并在该文件的package_info内添加(<emap_version>1.8.30.B106</emap_version>),用于自动部署。若不需要自动部署则不需要添加这段代码。
![](/assets/app_info.png)
4. permission.xml（必须）文件则询问相关人员拿到，也放入根目录。
5. 通过源代码打包，打包命令：npm run deploy。这个命令会在项目目录下生成一个 zip 包，zip 包的名字就是在初始化项目脚手架的时候询问的名字（可在package.json文件中修改相关信息）。打完包记得解压然后把公共服务特有的"com"文件夹拷贝到classes目录下，重新打包的时候注意压缩包压缩方式（直接在项目内选中所有内容右键压缩）。
6. 在刚才新建的应用，点击 进入开发环境 -> 应用包管理 -> 上传安装包 -> 接入管理 接入到对应测试环境。
7. 关于部署，分为两种：手动部署和自动部署。<br>
（1）手动部署，需要到云工场的[应用管理平台](http://crowdamp.wisedu.com/manage/index.html)下载安装包并到服务器上部署
![](/assets/crowdamp1.png) 
![](/assets/crowdamp2.png) 
（2）自动部署，需要到公共服务的[emap在线设计](http://crowdamp.wisedu.com/publicapp/sys/emapol/*default/index.do#/fbxx)去完成自动部署的操作。共分两种情况：首次上线和升级上线。<br>
-首次上线，是一个需要等待的事情，由于campusphere平台和emap在线设计平台的应用数据同步是在每天的零点进行。所以，在应用需要上线时需要在前一天先把应用创建好。注：只要新建应用就会同步不需要上传部署包和接入。
![](/assets/emapol1.png)
![](/assets/emapol2.png)
**注意：目前在‘获取并启用’过后，对于后端项目来说服务会自动重启，不需要再做别的操作。如果单纯更新web项目，需要线下去手动重启下服务。后续会解决这个问题** <br>
-升级上线，不需要等待，在上传部署包之后，记得重新接入一下就好。部署流程如下：<br>
首先到应用管理平台的系统管理->应用版本管理中心去做一下‘升级’操作
![](/assets/emapol3.png)
![](/assets/emapol4.png)
![](/assets/emapol5.png)
![](/assets/emapol6.png)
**注意：目前在‘获取并启用’过后，对于后端项目来说服务会自动重启，不需要再做别的操作。如果单纯更新web项目，需要线下去手动重启下服务。后续会解决这个问题**
8. 通知测试授权上线，测试部署成功之后可在今日校园客户端中打开， Crowd测试大学即是公共服务测试环境。

