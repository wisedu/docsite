
###直接上传组件：
表单外使用，上传后不需要再次保存操作，不存在token和临时文件的概念等：
参数：
```html
         @property {String/Array} [ftype=['jpg', 'png', 'jpeg']] 上传文件的类型限制
         @property {String/Number} [width=200] 展示图片的宽度
         @property {String/Number} [height=150] 展示图片的高度
         @property {Number} [limit=5] 上传数量限制
         @property {Number} [size=2048] 文件大小限制(Kb)
         @property {Boolean} [multiple=false] 是否支持多文件选择
         @property {String} [buttonType=button] - 按钮类型，block和button
         @property {String} [displayType=image] - 显示类型，file和image
         @property {String} [storeId=file] - 上传文件的类型
         @property {Array} imagesUrl - 已上传图片url的数组，用于对原有图片的展示
            支持两种方式设置原有数据：
            1,直接存储图片地址。格式：['http://图片1地址', 'http://图片2地址']
            2,存储对象：id为图片id，fileUrl代表图片路径。格式[{id: '001', fileUrl: 'htt...'}]
         @property {String} uploadUrl - 上传url
         @property {Object} uploadParam - 上传附加参数
         @property {String} deleteUrl - 删除url
         @property {Object} deleteParam - 删除附加参数
         @property {Boolean} readonly - 是否只读，默认false
         @property {Array} editButtons - 功能按钮，默认['download', 'preview', 'delete', 'reupload']
```

上传返回数据格式（必须字段）：
```html
    {
        success: true/false, //标记上传是否成功
        id: "465084e9ed85449fa717d661ae82722d", //后端使用
        name: 'image.jpg', //标记上传图片名称
        fileUrl: "http://xxx/image.jpg"//上传成功后的图片地址，用于显示图片
    }
```

兼容emap格式：
```html
    {
        code: 0,
        datas: {
            success: true,
            ……
        }
    }
```

删除图片时向后端发送图片id
删除返回数据格式（必须字段）
```html
    {
        success: true
    }
```


