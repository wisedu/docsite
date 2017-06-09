# DropdownTable 下拉表格

* 素材贡献：程良培
* 编辑：戚雨
* 2017-6-9

### 使用方式
* 在字段的显示类型中配置：下拉表格。并设置 数据获取地址

![](/assets/ddtable1.png)

* 数据获取地址：需要在页面配置中增加一个动作，用来为其提供数据

![](/assets/ddtable2.png)

![](/assets/ddtable3.png)

![](/assets/ddtable4.png)

* 如果配置完，在form中显示的与预期字段不一致（如下图显示的是WID），可以通过参数调整：

JSON参数里面进行显示字段与值字段的配置 {"displayMember":"name", "valueMember":"id"}

![](/assets/ddtable5.png)



