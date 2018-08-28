
# emapmUploadImgs

> 移动端上传/展示图片组件

----------


## 引入

```shell
走完了“快速上手”内的步骤，此处就不需要再引入，可直接使用
```

## 例子

组件单个使用情景
```html
<emapm-upload-imgs 
    :host-pathname='hostPathname' 
    :read-only='false' 
    :token="token" 
    :size="5000" 
    :max-number="9" 
    @on-token-change="onTokenChange"
></emapm-upload-imgs>
```
```javascript
data() {
    return {
        token: "", 
        hostPathname: 'http://crowdamp.wisedu.com/publicapp',//开发环境需要配置，生产环境如果不填默认取当前应用的域名前缀
    }
},
methods() {
    onTokenChange(val) { //监听上传组件内token的变化
        this.token = val;
    }
}
```
组件循环使用情景
```html
<emapm-upload-imgs 
    v-for='(item,i) in imgList'
    :index="i"
    :key="i"
    :host-pathname='hostPathname' 
    :read-only='true' 
    :token="item.token" 
    :size="5000" 
    :max-number="9" 
    @on-token-change="onTokenChange"
></emapm-upload-imgs>
```
```javascript
data() {
    return {
        imgList: [
            {
                token: ""
            },
            {
                token: ""
            }
        ], 
        hostPathname: 'http://crowdamp.wisedu.com/publicapp',//开发环境需要配置，生产环境如果不填默认取当前应用的域名前缀
    }
},
methods() {
    onTokenChange(val,index) { //监听上传组件内token的变化，获取当前操作的图片组件的索引
        this.imgList[index].token = val;
    }
}
```

## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| hostPathname  |  图片显示域名   | String    |     |   当前应用的域名前缀  |
| readOnly    | 是否只读 | Boolean | | false |
| token | 图片的对应token值 | String | | 空 |
| index | 当前图片组件在当前页面的索引值 | Number | | 0 |
| maxNumber | 允许上传的图片最大数量 | Number | | 9 |
| size | 允许上传图片的大小（KB） | Number | | 5000 |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| onTokenChange  | token值发生变化时触发 | val:双向绑定的token值；index:当前上传组件的索引值 |

