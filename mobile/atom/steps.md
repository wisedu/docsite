## Steps 步骤条

### 使用指南
``` javascript
import { Step, Steps } from 'bh-mint-ui2';

Vue.component(Step.name, Step);
Vue.component(Steps.name, Steps);
```

### 代码演示

#### 基础用法

```html
<mt-steps direction="horizontal">
    <mt-step status="finish">买家下单</mt-step>
    <mt-step status="error">商家接单</mt-step>
    <mt-step status="process">买家提货</mt-step>
    <mt-step>交易完成</mt-step>
</mt-steps>

```



#### 物流描述


通过`title`和`description`属性来定义物流描述信息


```html
<mt-steps
  icon-class="steps-success"
  title="物流进度"
  description="步骤的描述"
>
  <mt-step status="finish">买家下单</mt-step>
  <mt-step status="error">商家接单</mt-step>
  <mt-step status="process">买家提货</mt-step>
  <mt-step>交易完成</mt-step>
</mt-steps>
```


#### 竖向步骤条


可以通过设置`direction`属性来改变步骤条的显示方式

```html
<mt-steps direction="vertical" description="步骤的描述" title="物流进度">
    <mt-step>
        <h3>【城市】物流状态3</h3>
        <p slot="left">12:40<br>2016-07-12</p>
    </mt-step>
    <mt-step :status="status">
        <h3>【城市】物流状态2</h3>
        <p slot="left">10:00<br>2016-07-11</p>
    </mt-step>
    <mt-step status="process">
        <h3>【南京】快件发往南京中转站</h3>
        <p>快递发送中</p>
        <p slot="left">10:00<br>2016-07-11</p>
    </mt-step>
    <mt-step status="finish">
        <h3>【南京】快件已揽件</h3>
        <p>快递中心已收件，等待发送快递中心；已收件，等待发送快递中心已收件，等待发送；快递中心已收件，等待发送</p>
        <p slot="left">09:30<br>2016-07-10</p>
    </mt-step>
</mt-steps>
```





### Steps API

| 参数 | 说明 | 类型 | 默认值 | 可选值 |
|-----------|-----------|-----------|-------------|-------------|
| title | 当前步骤标题 | `String` | - | - |
| description | 当前步骤描述 | `String` | - | - |
| direction | 显示方向 | `String` | `horizontal` | `vertical` |
| iconClass | 状态图标样式 | `String` | - | - |
| padding-left | 垂直时，左侧区域 |`Number` | 150 |   |


### Step API

| 参数 | 说明 | 类型 | 默认值 | 可选值 |
|-----------|-----------|-----------|-------------|-------------|
| status | 当前步骤状态 | `String` | - | `finish` `process` `error` |




如：
```html
<mt-steps :padding-left="100">
  <mt-step status="process">默认区域</mt-step>
  <mt-step status="finish">
      <label>默认区域</label>
      <p slot="left">左侧区域</p>
  </mt-step>
</mt-steps>
```
