# 公有云常见问题 Q&A

### 文件上传相关

直接上传、分步上传 ...


### 今日校园原生请求[GET]发送方法

```javascript
BH_MOBILE_SDK.http.sendGetRequest(this.api, (response) => {
  if (response && response.code === 200) { // check http status
    try {
      let result = JSON.parse(response.data) // get result object
    } catch (e) {
      // handle parse error
    }
  } else {
    // handle wrong http status
  }
}, { // user defined headers
  'Content-Type': 'application/json'
})
```