###级联下拉：
级联下拉组件，可多级使用。

配置：
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

请求后台参数（第一级选择后会自动请求触发第二级的请求，后续类似）：
{
"searchValue":"[{\"name\":\"deptId\",\"value\":\"3\",\"builder\":\"equal\",\"linkOpt\":\"AND\"}]" //注意，searchValue的值是个字符串！
}

返回数据格式：
[{
    id: "45", 
    name: "汽车工程学院"
}]


###下拉树：
树状下拉列表，支持异步加载。

配置：
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
YMAL:
title:  '"required":true,"xtype":"tree","url":"/wec-user-mngt/code/dept","JSONParam": {"search": false}'
发回后台的请求参数：
{"pId":""} //第一次
{"pId":"45"} //异步展开某节点时
{"*tree":"1","searchValue":"汽车","checkParent":true} //搜索时

返回数据格式：
[{
    code: "000076",
    id: "45",
    isParent: 1, //代表其下是否有子级，值必须为0或1
    name: "汽车工程学院",
    pId: "1018650205222760"
}]



###直接上传组件：
    表单外使用，上传后不需要再次保存操作，不存在token和临时文件的概念等
    参数：
        参考组件文档

    上传返回数据格式（必须字段）：
        {
            success: true/false, //标记上传是否成功
            id: "465084e9ed85449fa717d661ae82722d", //后端使用
            name: 'image.jpg', //标记上传图片名称
            fileUrl: "http://xxx/image.jpg"//上传成功后的图片地址，用于显示图片
        }
        兼容emap格式：
        {
            code: 0,
            datas: {
                success: true,
                ……
            }
        }


        删除图片时向后端发送图片id
        删除返回数据格式（必须字段） 
        {
            success: true
        }



