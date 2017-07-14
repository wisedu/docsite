###级联下拉：
级联下拉组件，可多个配合使用。

配置：
```html
{
    "name":"deptId",
    "dataType":"string",
    "caption":"学院",
    "required":true,
    "xtype":"select",
    "url":"/wec-user-mngt/code/stuDept"
},
{
    "name":"majorId",
    "dataType":"string",
    "caption":"专业",
    "required":true,
    "xtype":"select",
    "url":"/wec-user-mngt/code/major",
    "linkageBy":"deptId",
    "linkageName":"deptId"
}
```

请求后台参数（第一级选择后会自动请求触发第二级的请求，后续类似）：
```html
{
"searchValue":"[{\"name\":\"deptId\",\"value\":\"3\",\"builder\":\"equal\",\"linkOpt\":\"AND\"}]" //注意，searchValue的值是个字符串！
}
```

返回数据格式：
```html
[{
    id: "45", 
    name: "汽车工程学院"
}]
```

###下拉树：
树状下拉列表，支持异步加载。

配置：
```html
{
    "name": "deptId", 
    "dataType": "string", 
    "caption": "部门", 
    "required": true, 
    "xtype": "tree", 
    "url": "/wec-user-mngt/code/dept", 
    "JSONParam": {
        "search": false  //配置是否显示搜索框
    }
}
```

YMAL:
```html
title:  '"required":true,"xtype":"tree","url":"/wec-user-mngt/code/dept","JSONParam": {"search": false}'
```
发回后台的请求参数：
```html
{"pId":""} //第一次
{"pId":"45"} //异步展开某节点时
{"*tree":"1","searchValue":"汽车","checkParent":true} //搜索时
```

返回数据格式：
```html
[{
    code: "000076",
    id: "45",
    isParent: 1, //代表其下是否有子级，值必须为0或1
    name: "汽车工程学院",
    pId: "1018650205222760"
}]
```




