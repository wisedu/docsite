## 微信企业号js-sdk调用

示例 [demo](http://res.wisedu.com:8888/demo/)

官方文档 [地址](http://qydev.weixin.qq.com/wiki/index.php?title=%E9%A6%96%E9%A1%B5)

signature信息获取接口

```javascript
$.ajax({
  type: 'POST',
  url: 'http://res.wisedu.com:8888/checkSign',
  data: {
    url: window.location.href.replace(/#(\S+)?/, '')
  },
  success: function (res) {
    // do sth
  }
})
```
其中，res的结构为
```javascript
{
  status: '0',
  data: {
    jsapi_ticket: 'kgt8ON7yVITDhtdwci0qeZfUO_fgLidT9Siy7h9fwEUMkbXHNCo9E6qpAZeQPXH6sdaZ6tgtzNraNmFzeIXV-w',
    nonceStr: '2g2oo1tozs9bxt8',
    signature: '33328095346149d69173e2be4c7ecf431ace188d',
    timestamp: '1492046620',
    url: 'http://res.wisedu.com:8888/demo/'
  }
}
```
    
