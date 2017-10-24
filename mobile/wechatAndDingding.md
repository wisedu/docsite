## 微信与钉钉集成环境文档
注意：本文中的微信环境特指微信服务号

## 关键词1：开发

问题1：大家了解什么是验证jssdk以及为什么要验证jssdk吗?
答：当前网页有没有资格调用微信的接口

###集成了什么？

一个叫bh-mixin-sdk的node-modules包。
![](/assets/wxdd-package.json.png)

对外暴露的是一个SDK的全局变量

此包的作用：1、提供今日校园的全部api

2、进行微信钉钉的jssdk验证，并提供公共基础类接口

###代码内用法

脚手架内main.js内需要我们根据自己项目配置的地方：
![](/assets/wxdd-main.js.png)
代码里配置的事例：微信vs钉钉
![](/assets/wxdd-config.js.png)
因为-----------------------------------------------------我们兼容两种写法。一种传url，一种传signData。
如果以url方式验证,我们希望验证jssdk的接口以这个格式返回：
![](/assets/wxdd-jssdk-api.png)

如果以signData方式，就只能通过脚手架内的utils.Get自己来获取了。

当然我们希望你的signData是这个格式的：
![](/assets/wxdd-signdata.png)

微信jssdk相关的文档 

狠狠戳这里：https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1421141115 

钉钉jssdk相关的文档

狠狠戳这里：
https://open-doc.dingtalk.com/docs/doc.htm?spm=a219a.7629140.0.0.5ZZdb2&treeId=171&articleId=107553&docType=1 

###如何调用api呢？
![](/assets/wxdd-jssdk-sdk.png)


我们看到了global.SDK。公共基础类的api 无论是今日校园、微信还是钉钉都通过

SDK.setTitleText(‘我要飞’);

如果单独调用非基础类微信的接口，你需要这样：
![](/assets/wxdd-wx-api.png)

如何查到调用微信api的用法？

狠狠戳这里：https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1421141115 

如果单独调用非基础类钉钉的接口，你需要这样：
![](/assets/wxdd-dd-api.png)

如何查到调用钉钉api的用法？

狠狠戳这里：
https://open-doc.dingtalk.com/docs/doc.htm?spm=a219a.7629140.0.0.5ZZdb2&treeId=171&articleId=107553&docType=1 

##关键词2：调试

###微信
微信开发者工具
https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1455784140 

###钉钉
钉钉调试
https://open-doc.dingtalk.com/docs/doc.htm?spm=a219a.7629140.0.0.RgZo5o&treeId=171&articleId=104908&docType=1 

##关键词3：部署

###微信环境（微信服务号）

1、是否有服务号，是-请跳第二步，否-请继续看。
申请步骤：https://jingyan.baidu.com/article/e9fb46e190a51a7521f766d7.html 

营业执照注册号
营业执照副本扫描件
![](/assets/wxdd-wx-fwh.png)


2、是否完成服务号服务器配置，是-请跳转第三步，否-请继续看
配置步骤：https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1421135319 

为什么要配置？
![](/assets/wxdd-wx-dev.png)



3、是否设置白名单，是-跳第四步，否-请继续看

![](/assets/wxdd-wx-fwh-config.png)
![](/assets/wxdd-wx-ip.png)


通过开发者ID及密码调用获取access_token接口时，需要设置访问来源IP为白名单。
A:什么是开发者id与密码？见上图
B：access_token是什么，有什么用？ 
https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1421140183
C：换句话说，非ip白名单内的ip地址，请求access_token时获取不到！！不到！！也就是你必须把应用正式环境以及开发环境的ip全部添加到白名单！！！！！！！

为什么做ip白名单设置：
https://mp.weixin.qq.com/cgi-bin/announce?action=getannouncement&key=1495617578&version=1&lang=zh_CN&platform=2 


4、验证微信jssdk（“失物招领”应用里面需要用到上传预览图片的api）
https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1421141115 



###钉钉环境

1、打开钉钉管理后台

https://oa.dingtalk.com/index.htm#/login 

2、登录
![](/assets/wxdd-dd-login.png)
![](/assets/wxdd-dd-workspace.png)
![](/assets/wxdd-dd-addApp.png)


钉钉的文档
https://open-doc.dingtalk.com/?spm=a2115p.8777639.4570797.3.1c474d72QMm4bW 

钉钉jssdk的验证
https://open-doc.dingtalk.com/docs/doc.htm?spm=a219a.7629140.0.0.uB1Zin&treeId=171&articleId=104910&docType=1 


钉钉接口概览
https://open-doc.dingtalk.com/docs/doc.htm?spm=a219a.7629140.0.0.fCgqQ5&treeId=171&articleId=106834&docType=1 
分为两类，基础类无需jssdk验证就可以调用，而另一类测试需要验证的。

钉钉调试
https://open-doc.dingtalk.com/docs/doc.htm?spm=a219a.7629140.0.0.RgZo5o&treeId=171&articleId=104908&docType=1 