# RES - Wisedu FE


## 目前公司的res环境有如下几套：
1. http://res.wisedu.com/ver/next/ 这套为公司的RES开发环境地址，云内云外均可以访问；但其中包括未经测试的最新功能，也可能含有bug，使用这些功能时，存在风险。
1. http://res.wisedu.com/ver/1.8.0_EM4/ 带有某一固定的版本号，为公司内测试已发版的RES环境地址，云外可以访问，该内容是通过测试，已发版的代码，也是目前可用的最新版本的功能。
1. http://cdnres.campusphere.cn 特别提醒，这套为仅针对 移动端 使用的RES服务器，仅云外可以访问，正常情况下即使在现场也不用修改该地址。


## 对各类人员而言：
### 产品线开发人员（以及测试人员）：
1. 建议优先选择使用 http://res.wisedu.com/ver/某一固定版本/ ，且应当在现场实施人员可修改的配置文件中配置（而不可写死）；
1. 虽然也可使用https://res.wisedu.com ，但务必注意此环境中包括未经测试的最新功能，也可能含有bug，因此转测试前、发布版本前要特别考虑此处是否改为引用 http://res.wisedu.com/ver/某一固定版本/ （如果不修改，请务必考虑可能存在此问题：已经发布了的版本，到了现场却发现学校的res网站都没有这个功能，从而无法使用的问题）。
1. 如果有移动端，则移动端功能使用的RES地址为 http://cdnres.campusphere.cn ，正常情况下，现场不用修改该地址。


### 现场实施人员：
1. 产品发布的版本中，对相应的RES静态资源服务器应当均有该配置，
1. 一般情况下，当部署到现场的时候，需要调整RES地址为该学校RES服务器地址，如：南农 res.njau.edu.cn。
1. 其中，如果有移动端，则移动端功能使用的RES地址为 http://cdnres.campusphere.cn ，正常情况下，现场不用修改该地址。

## 请各位务必注意保证，现场环境 \[_不可以_\] 连接以下地址：
* https://res.wisedu.com



# 金智教育前端团队

## 前端读物

请访问：[https://res.wisedu.com/FS/前端入门/](https://res.wisedu.com/FS/前端入门/)  
文件前面的编号为难度等级

从零学习前端开发：[https://zhuanlan.zhihu.com/p/22099626](https://zhuanlan.zhihu.com/p/22099626)  
前端入门四弹：[https://zhuanlan.zhihu.com/p/21551062](https://zhuanlan.zhihu.com/p/21551062)


## 团队成员

[elvisqi](https://github.com/elvisqi): Going to bed at night saying we've done something wonderful... that's what matters to me

@qdli: 真正的勇士，敢于直面惨淡的warning，敢于直面淋漓的error！！！

张丹   知之为知之，不知为不知，是bug也

[GilbertSun](https://github.com/GilbertSun) 我们的征途是星辰大海！！！！

[lordrobert](https://github.com/lordrobert) 怒粘四海代码，笑写八荒业务

[lkiarest](https://github.com/lkiarest)  觉宇宙之无穷，识盈虚之有数

zhufeifei:  test

[lisiur](https://github.com/lisiur) 我牛不牛逼我不知道，但是当别人跟我说：“你死了地球照样转”的时候，我觉得地球是在硬撑着。

[litor](https://github.com/Litor)为API生，为框架死，为debug奋斗一辈子，吃符号亏，上大小写的当，最后死在需求上

[zhroeqqtw](https://github.com/zhroeqqtw) 我这边是好的啊，你清缓存刷新一下试试！

[zenda96](https://github.com/zenda96/)
世界上有10种人，一种是懂二进制的人，一种是不懂二进制的人

[GongYoo](https://github.com/GongYoo) 此处功能将来必改，不要写死!

[liwenjie](https://github.com/liwenjie3421) what's up!

[wengqi](https://github.com/wengqi) 简约至上

[qylin](https://github.com/qylin) 醉生梦死

[xujiabin](https://github.com/js-nj) 插播广告，王者荣耀，微信区，黄金级别，欢迎加好友，一起开黑
