# Command Bar

> 命令按钮，支持更多按钮显示，一般用于流程审批

-------------

## 引入

```javascript
import { CommandBar } from 'bh-mint-ui2';

Vue.component(CommandBar.name, CommandBar);
```

## 例子

```html
<template>
  <mt-command-bar :buttons="buttons" :more-buttons="moreButtons"></mt-command-bar>
</template>

<script>
  export default {
    data() {
      return {
        buttons: [
            {name:"退回",id:"tuihui", type:"default"},
            {name:"提交",id:"tijiao", type:"default"},
            {name:"启动",id:"qidong", type:"primary"}
        ],
        moreButtons: [{name:"同意"},{name:"终止"},{name:"流程状态"}]
      };
    }
  };
</script>
```


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 | 示例值 |
|------|-------|---------|-------|--------|--------|
| buttons | 平铺按钮 | Array |  | [] | [{name:"退回",id:"tuihui", type:"default"}] |
| more-buttons | 更多按钮 | Array | | [] | [{name:"同意"}] |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click  | 点击项后触发 | `项`,`顺序值`,`原始dom事件`  |

<script>
  export default {
    data() {
      return {
        buttons: [
            {name:"退回",id:"tuihui", type:"default"},
            {name:"提交",id:"tijiao", type:"default"},
            {name:"启动",id:"qidong", type:"primary"}
        ],
        moreButtons: [{name:"同意"},{name:"终止"},{name:"流程状态"}]
      };
    }
  };
</script>
