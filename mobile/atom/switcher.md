# Switcher

> 切换按钮

-------------

## 引入

```javascript
import { Switcher } from 'bh-mint-ui2';

Vue.component(Switcher.name, Switcher);
```

## 例子

`label` 属性为切换按钮的名称。

`v-model` 属性为切换按钮的当前值。



```html
<template>
  <mt-switcher
    label="标题"
    v-model="value1"
    @change="handleChange">
  </mt-switcher>
</template>

<script>
  export default {
    methods: {
      handleChange(event) {
        //切换后的回调函数
        console.log(event)
      }
    }
  };
</script>
```


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| label | 切换按钮文件列表的名称 | String | | '' |
| v-model | 切换按钮的初始值 | Number | | 0 |


## Events
| 事件名称 | 说明 | 回调参数 |
|------|-------|---------|
| change | 切换按钮变化时的回调函数 |  |

<script>
  export default {
    data: function(){
      return {
        value1:""
      }
    },
    methods:{
      handleChange(event) {
        //切换后的回调函数
        console.log(event)
      }
    }
  };
</script>
