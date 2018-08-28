# Tabbar

> 底部选项卡，点击 tab 会切换显示的页面。依赖 tab-item 组件。

-------------

## 引入

```javascript
import { Tabbar, TabItem } from 'bh-mint-ui2';

Vue.component(Tabbar.name, Tabbar);
Vue.component(TabItem.name, TabItem);
```

## 例子

搭配 <router-link :to="{ path:'/' + $route.meta.language + '/tab-container' }">tab-container</router-link> 组件使用

选用字体库图标（推荐使用）
```html
<mt-tabbar v-model="selected" fixed>
  <mt-tab-item id="外卖" icontype="home">
    外卖
  </mt-tab-item>
  <mt-tab-item id="订单" icontype="lingdaorichengicon">
    订单
  </mt-tab-item>
  <mt-tab-item id="发现" icontype="lingdaorichengicon">
    发现
  </mt-tab-item>
  <mt-tab-item id="我的" icontype="wodezixun">
    我的
  </mt-tab-item>
</mt-tabbar>
```

自定义图标
```html
<mt-tabbar v-model="selected" fixed>
  <mt-tab-item id="外卖" >
    <img slot="icon" src="../assets/100x100.png">
    外卖
  </mt-tab-item>
  <mt-tab-item id="订单" >
    <img slot="icon" src="../assets/100x100.png">
    订单
  </mt-tab-item>
  <mt-tab-item id="发现" >
    <img slot="icon" src="../assets/100x100.png">
    发现
  </mt-tab-item>
  <mt-tab-item id="我的" >
    <img slot="icon" src="../assets/100x100.png">
    我的
  </mt-tab-item>
</mt-tabbar>
```

选用徽章（dot,figure）
```html
<mt-tabbar v-model="selected" fixed>
  <mt-tab-item id="红点" icontype="home"  badge="dot">
    红点
  </mt-tab-item>
  <mt-tab-item id="数字" icontype="wodezixun" badge="figure" badgeValue="99+">
    数字
  </mt-tab-item>
</mt-tabbar>
```

自定义徽章（需要自定义样式）
```html
<mt-tabbar v-model="selected" fixed>
  <mt-tab-item id="红点" icontype="home" >
    <mt-badge size="small" padding="3px" type="danger" slot="badge"></mt-badge>
    红点
  </mt-tab-item>
  <mt-tab-item id="数字" icontype="wodezixun">
    <mt-badge size="small" type="danger" slot="badge">99+</mt-badge>
    数字
  </mt-tab-item>
</mt-tabbar>
```


## API

### tabbar
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| fixed | 固定在页面底部 | Boolean | | false |
| value | 返回当前选中的 tab-item 的 id | * | |  |


### tab-item
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| id | 选中后的返回值 | * | |  |
| icontype | 选用的字体图标名称 | String | 参看字体图标 |  |
| badge | 可选内置徽章类型 | String | `dot`,`figure` | '' |
| badgeValue | 内置徽章为`figure`状态下的填充值 | String,Number | - | - |

## Slot

### tabbar
| name | 描述 |
|------|--------|
| - | 内容 |

### tab-item
| name | 描述 |
|------|--------|
| - | 显示文字|
|icon | icon 图标，用于插入图片（与icontype效果相同，两者可选其一）|
|badge | badge 徽章,存在内置（dot,figure）两种,也可自定义,但需要对样式进行修改 |



<script>
  export default {
    data: function(){
      return {
        selected:"外卖"
      }
    },
    methods:{
    }
  };
</script>
