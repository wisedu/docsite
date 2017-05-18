
<!-- # 1.7.1_TR3
qiyu 2017-3-21 解决 type=confirm 时，dialog的背景无颜色

改了ubase
qiyu 2017-3-21 type会作为dialog的背景颜色，传递confirm导致对话框背景无颜色
 -->

# 1.7.1_TR6

bug
1. 助学金】助学金审核，审核统计，关闭按钮上方给了一条半截的线条 http://jira.product.wisedu.com/browse/XG-3780
2. 助学金】助学金管理，新增，基本信息，编辑框空格没有过滤，名额可为负数 http://jira.product.wisedu.com/browse/XG-3615
3. 【助学金】助学金种类，新增，名额编辑框不能编辑 http://jira.product.wisedu.com/browse/XG-3774

# 1.7.1_EM5
需求：
1.	表格组件请求数据，修改请求响应的code的判断方式，兼容老版本应用，对code不存在的情况做兼容处理，不再弹出错误提示


# 1.7.1_TR4
需求
1. 添加 下拉表格querySetting的 传参方式
2. 条件构造器中下拉树最多选择1000项 http://jira.product.wisedu.com/browse/RES-274
3. 只读文本域添加高度自适应功能 http://jira.product.wisedu.com/browse/XQGL-1656
4. 上传组件 增加CPT格式的图标 http://jira.product.wisedu.com/browse/RES-273
bug
1. 修改表单日期范围清空的问题
2. 【智校云-配置中心】新建业务表单，列表中显示的数据不是新建时配的，见附图 http://jira.product.wisedu.com/browse/SAAS-1175
3. bh_choose组件在启用searchByQuerySetting模式下，清空查询条件后，querySetting未清空，导致查询结果不对 http://jira.product.wisedu.com/browse/RES-256
4. 【学生管理队伍】选择任职开始日期、任职结束日期点击搜索无效 如图 http://jira.product.wisedu.com/browse/XG-3422
5. 【学生申请】学生端申请详情审核状态与申请信息重叠 如图	http://jira.product.wisedu.com/browse/XG-3538
6.  emap表单下拉树联动下拉框bug	http://jira.product.wisedu.com/browse/RES-272
7.  IE9下操作异常，无法选中人员 http://jira.product.wisedu.com/browse/XG-3600
9.  生源核对：院系负责人编辑页面，职工号显示不明显 http://jira.product.wisedu.com/browse/JY-140
10. 【社会考试报名管理】【考试项目管理】【限制条件】成绩输入负数可以保存成功 http://jira.product.wisedu.com/browse/JW-1942


 
# 1.7.1_EM3L

需求：

下拉树性能优化，需要同步加载3500条数据，不出现卡顿
bug：

RS-3387 高级查询和条件构造器组件树形菜单选择异常

# 1.7.1_TR2
需求：
1. 滚轮只需支持纵向滚动条，不要支持横向滚动条 http://jira.product.wisedu.com/browse/RES-249 用例： http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/xsxxddwh
1. 添加全选反选项功能 http://jira.product.wisedu.com/browse/XG-3075
1. 自定义显示列弹窗功能完善 http://jira.product.wisedu.com/browse/RS-3258 用例： http://demoapp.wisedu.com/emap/sys/student_app2/*default/index.do#/customColumn
1. 【头像裁剪上传】组件不支持临时文件保存 http://jira.product.wisedu.com/browse/RES-254
1. 大文本输入框需支持默认高度 http://jira.product.wisedu.com/browse/UED-403 用例： http://res.wisedu.com/examples/components-v1/bhTxtInput/bhTxtInput.html
2. 表格列宽设计修改 http://jira.product.wisedu.com/browse/UED-462
3. 自定义显示列迭代 http://jira.product.wisedu.com/browse/RES-259 用例：  http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/xsxxddwh


bug：
1. 提示信息全部移到最上方 http://jira.product.wisedu.com/browse/JW-1803
2. 【学籍异动】【学籍异动查询】ie9兼容问题：切换到高级查询页面查询条件下拉框提示信息丢失 http://jira.product.wisedu.com/browse/YJS-550
4. 新生信息管理】-【新生信息管理】编辑或添加或查看时信息项收起，下方显示空白 http://jira.product.wisedu.com/browse/YJS-577
5. 组合查询结果不正确（任职信息查询） http://jira.product.wisedu.com/browse/XG-3348
6. 【公共】高级查询选择字段、条件和字段值，点击清空按钮，字段值未清空 http://jira.product.wisedu.com/browse/YJS-638

# 1.7.1_TR1

需求
1. 表格列宽可以手动设置到100以下，若未设置，则保持最小列宽100并自适应  用例：http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/xsxxdbwh
2. 高级搜索 条件构造器 条件搜索 高级搜索2.0 中的下拉 多选下拉 下拉树 选下拉树添加空值选项  http://jira.product.wisedu.com/browse/RES-244
 用例：http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/xsxxdbwh
http://demoapp.wisedu.com/emap/sys/student_app2/*default/index.do#/filterQuery
http://demoapp.wisedu.com/emap/sys/student_app2/*default/index.do#/emapQuery
3. 表单只读和编辑混排填写提示 http://jira.product.wisedu.com/browse/RES-245 用例 http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/tableForm 
4. 新增进度条原子组件 http://jira.product.wisedu.com/browse/RES-234 用例 http://res.wisedu.com/examples/components-v1/bhProgressBar/bhProgressBar.html?min=1
5. 条件构造器组件改造 http://jira.product.wisedu.com/browse/RES-248  人事综合查询
6. 表格增加defaultParam参数 
7. 前端组件1.2版本，新增emapForm 数字区间类型取值为小数的功能 http://jira.product.wisedu.com/browse/JW-1575
8. 新增7种皮肤方案
bug 
1. 数字区间问题 http://jira.product.wisedu.com/browse/RES-242
3. [表单校验]表单校验在必填校验生效后，将字段设置为非必填，校验样式仍然存在 http://jira.product.wisedu.com/browse/RES-247
4. 【新生信息管理】-【新生信息管理】查询条件籍贯读取有问题 http://jira.product.wisedu.com/browse/YJS-367
6. 【就业职位】发布时间显示问题 如图 ttp://jira.product.wisedu.com/browse/XG-2971
7. 2.0block展示方式（单个带title）:第一次上传附件展示的不是设置的title，而是附件的title；重新上传的菜展示设置的title http://jira.product.wisedu.com/browse/RES-252
8. 教职查询统计_v4.0.5_IE9兼容问题：（1）条件构造器没有提示文字（2）选择条件不默认【等于】，一直是选择条件（3）无法创建查询条件（4）到处选择字段搜索框也没有提示字样 http://jira.product.wisedu.com/browse/RS-3270
9. 教职工综合查询_v4.0.5_（1）条件配置页面设置里的字段选择勾选去掉后，字段也消失（2）字段页面有两个表名字段，不太合理（3）教职工查询页面自定义列显示也存在同样问题 http://jira.product.wisedu.com/browse/RS-3265

# 1.7.0_EM7
bug

# 1.7.0_TR6

1.  crowd 前端控件高级搜索功能失效 http://jira.product.wisedu.com/browse/RES-240

# 1.7.0_TR5

需求：
1. 上传头像图片修改时，调用ＥＭＡＰ保存图片需要添加三个参数 http://jira.product.wisedu.com/browse/YJS-217  用例： http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/avatar
2. 添加扩展校验规则方法  extendValidateRule 用例： http://demoapp.wisedu.com/emap/sys/student_app2/*default/index.do#/editForm
3. 模型配置允许给字段添加多个校验规则， 用,分隔  
4. bh_choose组件需改造查询条件到querySetting http://jira.product.wisedu.com/browse/RES-233 用例：http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/choose
6. 上传下载组件自定义操作（数量，内容）支持 http://jira.product.wisedu.com/browse/RES-230 用例： http://demoapp.wisedu.com/emap/sys/student_app2/*default/index.do#/upload
7. 文本域需在填写和只读时支持自适应文本高度，并设置最大高度，现添加参数autoHeight,默认false http://jira.product.wisedu.com/browse/RES-228 用例：http://res.wisedu.com/examples/components-v1/bhTxtInput/bhTxtInput.html
8. 高级搜索，在执行搜索前，增加beforeSearch回调，返回false则阻断搜索 http://jira.product.wisedu.com/browse/JW-1212 用例：http://demoapp.wisedu.com/emap/sys/student_app2/*default/index.do#/advancedQuery
9. res 添加数据采集功能， 直接对接 emappagelog, 采集用户行为数据
10. BH_UTILS.doAjax， 增加requestOption请求配置
11. pdf预览时，不要截取文件名，通过流读取时，显示的相似乱码，需求人：刘弋 用例： http://localhost:8080/emap/sys/student_app1.2/*default/index.do#/upload



bug：
1. 【单位审核与管理】单位图册可以上传10张 如图 http://jira.product.wisedu.com/browse/XG-2768
2. 各类人员管理-导入，导入模板使用错误的情况下，提示信息不够友好，仅提示导入失败 http://jira.product.wisedu.com/browse/RS-3131
3. 【学生住宿】住调退，高级搜索，设计到搜索学号逗号隔开的，空格和特殊字符需要过滤 http://jira.product.wisedu.com/browse/XG-2760
4. 【排课管理】参数设置页面拉至下面时菜单栏显示有误 http://jira.product.wisedu.com/browse/JW-1264
5. 【学籍异动设置】【异动类型】字段显示及维护配置tab页显示修改 （调整开关disable颜色）http://jira.product.wisedu.com/browse/YJS-326
6. 教职工信息上报-ie9浏览器，自定义列搜索框内没有提示文字 http://jira.product.wisedu.com/browse/RS-3158
7. 修改字典定义、修改和新增字典时，描述的输入框显示最大输入500个字符，但是校验不正确，提示也不正确 http://jira.product.wisedu.com/browse/ESOP-145
8. YYGLPT-928
【应用管理】设置为每页显示50条，页面下拉至底端，点击右上角展开用户信息，再上拉页面，右上角弹框跟着页面一起滚动

# 1.7.0_EM4
 南理工现场临时版， 基于1.7.0_TR1添加数据收集功能

# 1.7.0_TR3
需求：
1. 高级搜素下拉树勾选父节点需要联动选中所有子节点 http://jira.product.wisedu.com/browse/RES-207
2. emapform渲染的时候集成1.2上传下载组件
 http://jira.product.wisedu.com/browse/RES-226

bug： 
1. 单个表单字段校验报错问题
2. 表格表单下radio下边距调整
3. 【新生信息管理】学生查询输入值收起后有问题 http://jira.product.wisedu.com/browse/YJS-165
4. 【新生信息管理】查询条件部分日期控件和下拉值无法维护 http://jira.product.wisedu.com/browse/YJS-164
5.  【新生信息管理】更多条件已选择搜索字段统计数量错误 http://jira.product.wisedu.com/browse/YJS-163
6.  【新生信息管理】单个添加页面，页面字段排版需要调整，涉及到地址的两格显示，家庭成员需大文本显示 http://jira.product.wisedu.com/browse/YJS-146
7.  【新生信息管理】切换到高级查询，选择值为下拉值形式的字段，清空时无法清空字段值 http://jira.product.wisedu.com/browse/YJS-132
8.  【新生信息管理】单个添加学生时，右侧字段总数统计不正确 http://jira.product.wisedu.com/browse/YJS-128
9.  【新生信息管理】单个添加学生时，必填项未填写，建议保存后跳转到必填项 http://jira.product.wisedu.com/browse/YJS-126
10.  【基本信息】审核统计进入会弹出是否执行2，在批次设置中展示执行后的结果 http://jira.product.wisedu.com/browse/XG-2681
11.  【宿舍卫生】卫生管理，查看详情中的图片，下拉条在抖动 http://jira.product.wisedu.com/browse/XG-2621
12.  【宿舍卫生】卫生管理，新建宿舍编辑分数为负数时，提示语是否要修改 http://jira.product.wisedu.com/browse/XG-2603
15.  考勤管理：选择考勤管理月份，页面数据不更新 http://jira.product.wisedu.com/browse/RS-3083
16.  考勤管理：存在增加缺勤信息，组件中时间无法选中的情况 http://jira.product.wisedu.com/browse/RS-3078
17.  教职工信息变更：无附件的情况下，点击附件打开空白页面，需优化 http://jira.product.wisedu.com/browse/RS-3061
18.  教职工信息变更：工作经历附件上传有问题 http://jira.product.wisedu.com/browse/RS-3057
19.  高级搜索【再次执行高级搜索，下拉框有值，内容框没值】http://jira.product.wisedu.com/browse/RS-3054
20.  岗位聘任-个人端附件上传（1）上传有时候上传不了，一直在转（2）上传取消，显示上传临时文件失败（3）上传的图片有时候显示是破损的（4）附件下载越权 http://jira.product.wisedu.com/browse/RS-3048
21.  岗位聘任-高级搜索保存为方案后，执行该方案后列表中不显示数据，正常搜索下是有数据的 http://jira.product.wisedu.com/browse/RS-2973
22.  岗位聘任-附件显示问题 http://jira.product.wisedu.com/browse/RS-2971
23.  表格组件固定列宽后导致表格标题样式异常 http://jira.product.wisedu.com/browse/RES-224
24.  编辑表格数字校验，组件报错 http://jira.product.wisedu.com/browse/RES-223
25.  validate BUG http://jira.product.wisedu.com/browse/RES-221
26.  表单边框颜色显示异常 http://jira.product.wisedu.com/browse/RES-220
28.  emapDropDownTree加载时间长时，没有等待提示，误认为点击没响应 http://jira.product.wisedu.com/browse/RES-159
29.  考勤管理：考勤详情页面添加缺勤，选择一个考勤类别，页面显示系统异常 http://jira.product.wisedu.com/browse/RS-3082
30.  教职工信息管理-扩展信息管理：添加和删除附件不成功及页面展示出现问题（重现率约50%） http://jira.product.wisedu.com/browse/RS-3051
31.  岗位聘任-个人端，请求token加载失败 http://jira.product.wisedu.com/browse/RS-3085
32.  【排课管理】班级/教室/教师课表查看列表全选之后切换每页显示数量后页面显示有误 http://jira.product.wisedu.com/browse/JW-1186
33.  【学籍信息管理】-【照片管理】批量导入，重新上传后文件名称仍为之前文件的名称 http://jira.product.wisedu.com/browse/YJS-240

# 1.7.0_TR2

bug
1. 【宿舍卫生】卫生管理，上传错误的文档提示undefined http://jira.product.wisedu.com/browse/XG-2598
2.  请假管理-个人端选择请假日期后，请假天数不会自动生成 http://jira.product.wisedu.com/browse/RS-2959
3.  下拉树排序问题 http://jira.product.wisedu.com/browse/RES-206
4.  【宿舍违纪】-宿舍违纪下面违纪类型设置新增成功一会会拉长，关闭就是好的 http://jira.product.wisedu.com/browse/XG-2584
5.  岗位聘用-个人填报端，字段较长样式问题 http://jira.product.wisedu.com/browse/RS-2990
6.  岗位聘用-部门审核端，个人信息详情界面样式错乱 http://jira.product.wisedu.com/browse/RS-3002
7.  时间范围组件，selectedTime事件获取的时间数据有问题 http://jira.product.wisedu.com/browse/RS-2995
8.  高级查询初始化事件init会在请求未完成时触发 http://jira.product.wisedu.com/browse/RS-1855
9.  【新生信息管理】查询条件部分日期控件和下拉值无法维护 http://jira.product.wisedu.com/browse/YJS-164
10.  【新生信息管理】学生查询输入值收起后有问题 http://jira.product.wisedu.com/browse/YJS-165
11.  【新生信息管理】更多条件已选择搜索字段统计数量错误 http://jira.product.wisedu.com/browse/YJS-163

# 1.7.0_TR1
需求：
1. 添加表单控件注入机制，可以自定义表单控件进行渲染
2.  新增四套皮肤包
3.  浏览器滚动条隐藏时留白 http://jira.product.wisedu.com/browse/XQGL-1560
4.  上传组件2.0 添加直接上传模式（默认不开启）， 直接保存为正式文件， 不需要再额外调用保存接口
6.  上传组件2.0 只读模式下支持多token预览 http://jira.product.wisedu.com/browse/RES-213
6.  添加新版校验组件bhValidate，替换现有jqxValidator 兼容现有应用 
7.  添加表格可编辑功能， 能够根据数据模型实例化不同的表单控件，并带有校验功能； 有添加一行功能
8.  添加新的树形组件bhTree， 基于zTree封装， 解决现有jqxTree组件渲染过慢的问题
9.  封装新的日期组件bhDateTimePicker(仅1.2版本)
10.  添加自定义列可排序功能 http://jira.product.wisedu.com/browse/YJS-76
11.  表格组件添加默认不加载数据配置项isOnceEmpty http://jira.product.wisedu.com/browse/YJS-75
12.  添加前端行为数据收集功能 sentry.js

bug： 
1. 联动检验，当联动项不存在时做兼容判断 http://jira.product.wisedu.com/browse/RS-2955

# 1.6.2_R8 
bug: 
1. 教职工招聘-（1）教职工招聘点击岗位申请，浏览器后退，前进，弹框不消失 http://jira.product.wisedu.com/browse/RS-2881
2. 日期控件中的英文显示成数字了 http://jira.product.wisedu.com/browse/XG-2546
3. 年度考核-条件构造器下编辑多值后复选框没有了 http://jira.product.wisedu.com/browse/RS-2919
4. 时间范围组件内存溢出 http://jira.product.wisedu.com/browse/RES-210
5. 年度考核-条件构造器组件选择时显示有问题 http://jira.product.wisedu.com/browse/RS-2922
5. 表单联动字段问题 http://jira.product.wisedu.com/browse/RES-211

# 1.6.2_R7
1. 表格组件checkbox全选时，忽略disabled的checkbox http://jira.product.wisedu.com/browse/YJS-2
2. 教职工招-高级搜索，添加搜索字段，出现的字段有的分类，有的未分类，根据什么分类的？？	RS-2863
3. 教职工招聘-下载准考证导入模板，不能出现表名属于安全问题 RS-2858
4. 教职工照片-IE10兼容性问题，纸质弹窗和页面重叠 RS-2805
5. 教职工招聘-招聘录用，勾选待录用的简历，点一下，勾选的简历消失 RS-2584

# 1.6.2_R6

bug:
1. ［学生住宿］学生申请记录，查看详情，关闭按钮此处有一条白线 http://jira.product.wisedu.com/browse/XG-2528
2. 【组件任务】下拉多选组件BUG  http://jira.product.wisedu.com/browse/XG-2525
3. ［兼容－学生出国］Safari，学生申请，申请的时间格式可以填写成2016.12.10 http://jira.product.wisedu.com/browse/XG-2505
4. ［兼容－学生出国］safari出国申请页面增加延期回国数据，延期回国按钮被页脚遮盖 http://jira.product.wisedu.com/browse/XG-2496
5. 【学生住宿】学校批次排宿，设置学生床位数，可用床位数输入负数失败 http://jira.product.wisedu.com/browse/XG-2485
6. 高级搜索，方案名称有特殊字符的，点击更多会报错 http://jira.product.wisedu.com/browse/XG-2469

# 1.6.2_R5

bug: 
1. 宿舍房源管理进入房源管理时，图片展示很慢 http://jira.product.wisedu.com/browse/XG-2321
2. 教职工招聘-发送通知时插入链接，页面显示有问题 http://jira.product.wisedu.com/browse/RS-2563
3. 时间组件当format为HH：mm时，日期组件还会显示 http://jira.product.wisedu.com/browse/GGFW-734
5. 学生出国出国申请，上传格式不正确的附件，提交时无任何提示 http://jira.product.wisedu.com/browse/XG-2380
6. 教职工招聘-招聘录用，勾选待录用的简历，点一下，勾选的简历消失 http://jira.product.wisedu.com/browse/RS-2584
7. 异动查询-查看人员基本信息列表显示有问题 http://jira.product.wisedu.com/browse/RS-2155
8. emapdatatable，将beforeSend函数中，传递给回调函数的参数：null -> arguments
9. 自定义列公共问题，自定义列分类展示，存在有一类没有勾选便无法保存的问题 http://jira.product.wisedu.com/browse/XG-2449
10. 【学生住宿】住宿审核，自定义显示列不全选无法保存 XG-2455
11. 自定义列公共问题，自定义列分类展示，存在有一类没有勾选便无法保存的问题 XG-2449
12. 【宿舍卫生】卫生查询高级搜索框默认提示信息过长导致显示不全 XG-2425
13. 【学生住宿】存在性别下拉框出现重复数据 XG-2421
14. 【宿舍卫生】卫生管理查看详情页面新增或编辑中上传附件数量超过限制时或文件类型不对时应保存不了 XG-2415
15. 【宿舍卫生】自定义列页面搜索提示不清晰，请设计给出解决方案 XG-2413
16. 搜索组件，分页显示有2个重复的页数 XG-2412
17. 宿舍卫生】卫生查询高级搜索保存为方案时有问题 XG-2408
18. 【宿舍卫生】卫生查询自定义显示列取消全选保存按钮不可点 XG-2404
19. 日期与时间的控件，时间部分的展示有问题 XG-2400
20. 班车服务-添加班车 指定发车时间 组件错乱 GGFW-697
21. 新进-自定义列前面的图标不见了  http://jira.product.wisedu.com/browse/RS-2711
22. 高级搜索，方案名称有特殊字符的，点击更多会报错 http://jira.product.wisedu.com/browse/XG-2469
23. 浮动组件，嵌入iframe时会报错

# 1.6.2_TR4


1. 组件添加对emap配置项jsonparam的支持 jsonParam http://jira.product.wisedu.com/browse/UED-268
2. 高级查询 默认模糊搜索builder兼容学工现有应用，将equal转为include http://jira.product.wisedu.com/browse/RS-2263
3. 保存方案优化 http://jira.product.wisedu.com/browse/XG-2310
4. emapdatatable 自定义列增加type为radio类型的自定义列 http://jira.product.wisedu.com/browse/JW-812 用例 http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/dataTable
5. 表单组件支持最新的上传组件，且上传组件的上传参数等可配置。 http://jira.product.wisedu.com/browse/RES-162
6. 通过模型渲染的下拉树组件需要添加是否允许勾选非叶子节点 http://jira.product.wisedu.com/browse/XQGL-1537  用例 http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/dropdownTree
7. 添加新的图标库
8. emapGrid 自定义列按钮修改图标和文字
9. 图片管理页面，上传的图片是否需要名字 http://jira.product.wisedu.com/browse/XG-2323

bug: 
1. 高级查询点击更多条件分组下的字段重复 http://jira.product.wisedu.com/browse/YJS-5
2. 关于应用打开添加高级搜索字段的弹框，建议统一样式 http://jira.product.wisedu.com/browse/XG-2309
4. 自定义显示列中没有勾选任何字段，确认按钮也应可点 http://jira.product.wisedu.com/browse/XG-2359
5.  文件排序，取消时页面图片排序不对 http://jira.product.wisedu.com/browse/XG-2357
6.  关于应用中新加的自定义显示列，不同应用展示还不一样，建议统一样式 http://jira.product.wisedu.com/browse/XG-2325
7.  IE浏览器，宿舍图片管理页面，缩略图大小不一致 http://jira.product.wisedu.com/browse/XG-2315
8.  关于学工当前高级搜索使用后的问题 http://jira.product.wisedu.com/browse/XG-2310
9.  关于应用打开添加高级搜索字段的弹框，建议统一样式 http://jira.product.wisedu.com/browse/XG-2309
10. 【IE9、10、11】敲backspace键、触发了浏览器的回退键 http://jira.product.wisedu.com/browse/JW-856
11.  自定义列应存在固定列 如图 http://jira.product.wisedu.com/browse/XG-2369

#1.6.2_TR3
功能：
1. 模糊查询使用配置的builder http://jira.product.wisedu.com/browse/RS-2263
1. 填报开始、结束时间建议鼠标插入到文本中日期组件即显示 http://jira.product.wisedu.com/browse/RS-2433
3. 提示弹窗需要支持异常码日志串行码展示 http://jira.product.wisedu.com/browse/RES-155
4. 字符串截取新增更多 收起效果 http://jira.product.wisedu.com/browse/RES-163
5.  dropDown组件支持根据浏览器边界自适应往上或往下弹出 http://jira.product.wisedu.com/browse/RES-164  用例： http://res.wisedu.com/examples/components-v1/bhDropdown/bhDropdown.htm
6.  上传组件排序功能 http://jira.product.wisedu.com/browse/RES-172

bug： 
1. 下拉表格getValue方法兼容 http://jira.product.wisedu.com/browse/RES-170
2. 相同日期不同时间点的填报时间，报填报结束时间不能早于填报开始时间 http://jira.product.wisedu.com/browse/RS-2429
3. 卡片列表页面不应该显示设置按钮 http://jira.product.wisedu.com/browse/RS-2309
4. 高级搜索添加字段中含有日期控件的添加今天跟清除按钮 http://jira.product.wisedu.com/browse/RS-2474
5. 高级搜索 保存方案功能 样式优化 http://jira.product.wisedu.com/browse/RES-171
6. 相同日期不同时间点的填报时间，报填报结束时间不能早于填报开始时间 http://jira.product.wisedu.com/browse/RS-2429 用例 http://demoapp.wisedu.com/emap/sys/student_app/*default/index.do#/validate
7. 设置页面取消勾选一个字段，全选勾号也应消失；还有设置里面的字段全都选中时全选前面的勾号应该显示 http://jira.product.wisedu.com/browse/XG-2298
8. 设置页面字段全不选时确认按钮不应不可点 http://jira.product.wisedu.com/browse/XG-2299
9. 离校登记管理高级搜索离校日期保存为方案没有保存成功 http://jira.product.wisedu.com/browse/XG-2305

# 1.6.2-TR2

功能： 
1. 下拉树前端搜索功能 http://jira.product.wisedu.com/browse/RES-160
2. 页脚浮动位置修改 http://jira.product.wisedu.com/browse/UED-248

# 1.6.2-tr1
功能：
  1. 表单组件重构 
  4. 高级搜索组件的model-url数据获取方式增加GET方式 http://jira.product.wisedu.com/browse/EMAP-197
  7. 导入组件添加参数 fileName http://jira.product.wisedu.com/browse/XG-1994
  8. formOutline添加抓取容器参数 http://jira.product.wisedu.com/browse/XQGL-1530
  9. 条件构造器组件添加一下保存为方案的功能 http://jira.product.wisedu.com/browse/XQGL-1519
  10.  表单日期范围组件
  
bug: 
1. 计数文本域高度变动 http://jira.product.wisedu.com/browse/RS-2156
2. ie按钮样式问题 http://jira.product.wisedu.com/browse/RS-2137
3. 附件丢失问题 http://jira.product.wisedu.com/browse/OA-109
4. 自定义显示列中不用显示checkbox字段 http://jira.product.wisedu.com/browse/RS-2090?filter=10974
5. 高级搜索k简单查询使用模型字段配置的defaultBuilder  http://jira.product.wisedu.com/browse/RS-2263
6. 高级搜索出生地，籍贯下拉框值显示重复（多选下拉书） http://jira.product.wisedu.com/browse/RS-2234


1. 显示开关按钮问题汇总、权限管理勾选错位问题 http://jira.product.wisedu.com/browse/XG-2151
2. 单图片上传 重新上传功能优化 http://jira.product.wisedu.com/browse/XG-2093
3. 只读文本域取值bug http://jira.product.wisedu.com/browse/RS-2385
4. 显示隐藏列设置字段全选后，再次打开后全选未被选中 http://jira.product.wisedu.com/browse/RS-2363
5. 绩效津贴-IE9兼容性问题，(1)新建津贴项的时候，项目类型和舍位方式的下拉菜单都掉到备注位置（2）并且版权信息一直在进行操作的时候闪跳，不合理 http://jira.product.wisedu.com/browse/RS-2345
6. 自定义显示列至少要选择一个字段 http://jira.product.wisedu.com/browse/RS-2268

# 1.6.1-TR3

bug： 
2. edge弹窗内表单多余线条http://jira.product.wisedu.com/browse/XG-1789  
1. 修改按钮绑定属性的侧边栏弹框，没有监听closeBefore方法，导致无法关闭弹框
2. 上传附件丢失问题 http://jira.product.wisedu.com/browse/OA-109
3. 字段设置不再checkbox http://jira.product.wisedu.com/browse/RS-2090
4. ie9  显示隐藏字段 弹窗中 文字过长截断处理 http://jira.product.wisedu.com/browse/RS-2049 

# 1.6.1-tr2
### 需求
1. XQGL-1486 展开时需要附加属性，简化判断

### bug
1. 表单赋值后触发校验报红的问题
  http://jira.product.wisedu.com/browse/XG-2039
2. qiyu 2016-10-13 RS-1854 表头与内容的边框计算方式不同，导致pinned列滚动时右侧无法加边框  http://jira.product.wisedu.com/browse/RS-1854
3. 纸质弹窗手动关闭时回调没有触发  http://jira.product.wisedu.com/browse/RS-1884
4. 表格表单 只读文本域赋值问题 http://jira.product.wisedu.com/browse/XG-2070
5. RS-1882 时间范围组件，显示的时间范围与初始化设定的时间不一致
6. XG-2078 多重纸质弹框，将子弹框关闭后，会将原本父层没有的页脚显示出来
7. 高级搜索删除日期范围字段前，销毁控件， 方式悬浮的下拉框依然展示在页面上 http://jira.product.wisedu.com/browse/RS-1139
8. 【兼容-基本信息】360安全，学生信息管理新增学生信息上传照片，照片内部出现编辑 http://jira.product.wisedu.com/browse/XG-2088
9. RS-1926 纸质弹框，忽略回调的参数不生效
10. 时间范围组件，当设置的类型是all的时候，第一次时间始终会显示的是当前时间的问题 RS-1882
11. 延迟50毫秒返回close回调,解决纸质弹框关闭后jqxtable显示宽度错误
12. 修改布局在IE9下的兼容问题，并添加4种布局的示例页
13. RS-1944 修改在IE9下的按钮无上边框问题
14. ie9 富文本编辑器 上传兼容 http://jira.product.wisedu.com/browse/RES-135



# 1.6.1-sp1 2016-10-09
### 需求

1. OA7.0sp南理工版本表单中上传的多个附件能换行显示,行高自适应调整 <http://jira.product.wisedu.com/browse/XQGL-1489>
3. 高级搜索 添加搜索字段 点击确认按钮 弹出 添加成功的tip弹框，若没有改动则不提示 http://jira.product.wisedu.com/browse/XG-1711

### bug

1. 表格表单 只读的textarea 赋值问题修复

  http://jira.product.wisedu.com/browse/XG-1957

  http://jira.product.wisedu.com/browse/XG-1960

1. 按钮组文字过多样式限制 <http://jira.product.wisedu.com/browse/XG-1766>

2. 正整数校验规则修改 <http://jira.product.wisedu.com/browse/XG-1837>

3. 在时间控件中时分秒控件点击后会乱跳 <http://jira.product.wisedu.com/browse/XG-1838>

4. 下拉搜索功能bug <http://jira.product.wisedu.com/browse/XG-1746>

5. 只读表单空字段getValue时返回空字符串，之前为undefined <http://jira.product.wisedu.com/browse/RS-1516>

6. 高级搜索 高级模式 日期范围选择组件 删除前 调用一次组件的destroy方法，防止下拉的弹窗没有及时销毁<http://jira.product.wisedu.com/browse/RS-1139>

9. 高级搜索下拉树实例化添加unblind:'/'参数，处理下拉树选项中名称显示异常的问题 http://jira.product.wisedu.com/browse/XG-1919
10. 下拉树联动下拉框时，筛选下拉框数据时，用的是下拉树的显示值，应该是代码值 http://jira.product.wisedu.com/browse/RES-142
11. 只读表单文字过多换行样式 http://jira.product.wisedu.com/browse/RS-1769
12. 只读表单中 文件上传控件 自动转化为 文件下载预览控件
    http://jira.product.wisedu.com/browse/XG-2027

# 1.6.1-tr1 2016-10-14

需求：

1. 上传组件重构，拆分出上传组件的视图模块与功能模块，并提供缓存上传与直接上传两种上传机制，添加接口适配层，适配公有云 <http://jira.product.wisedu.com/browse/RES-134>
2. 前端ajax请求返回403后页面一直无限刷新的场景处理，因安全整改后，权限机制调整，返回403后，不需要刷新当前页面，控制台打印日志即可 <http://jira.product.wisedu.com/browse/XQGL-1482>



2016-09-10

bug解决：
	1	表格不因为出现横向滚动条而出现纵向滚动条的问题
	2	固定表格高度情况下，表格因出现横向滚动条而不断变高
	3	出现三层及以上纸质弹窗时，关闭最顶级弹窗后，再打开纸质弹窗会出现样式错误

