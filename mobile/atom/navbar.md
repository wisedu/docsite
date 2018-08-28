# Navbar

> 顶部选项卡，与 <router-link to="tabbar">Tabbar</router-link> 类似，依赖 tab-item 组件。

------------

## 引入

```javascript
import { Navbar, TabItem } from 'bh-mint-ui2';

Vue.component(Navbar.name, Navbar);
Vue.component(TabItem.name, TabItem);
```

## 例子
搭配 <router-link to="tab-container">tab-container</router-link> 组件使用


```html
<mt-navbar v-model="selected" @change="change">
  <mt-tab-item id="1"  badge="dot">
    选项一
  </mt-tab-item>
  <mt-tab-item id="2" >
    <mt-badge size="small" padding="3px" type="danger" slot="badge"></mt-badge>
    选项二
  </mt-tab-item>
  <mt-tab-item id="3" >选项三</mt-tab-item>
  <mt-tab-item id="4" >选项四</mt-tab-item>
  <mt-tab-item id="5" >选项五</mt-tab-item>
  <mt-tab-item id="6" >选项六</mt-tab-item>
</mt-navbar>

<!-- tab-container -->
<mt-tab-container v-model="selected">
  <mt-tab-container-item id="1">
    <mt-cell-group>
      <mt-cell v-for="n in 20" :title="'内容 ' + n" wrapperpaddingleft="20px"/>
    </mt-cell-group>
  </mt-tab-container-item>
  <mt-tab-container-item id="2">
    <mt-cell-group>
      <mt-cell v-for="n in 10" :title="'测试 ' + n" wrapperpaddingleft="20px"/>
    </mt-cell-group>
  </mt-tab-container-item>
  <mt-tab-container-item id="3">
    <mt-cell-group>
      <mt-cell v-for="n in 6" :title="'选项 ' + n" wrapperpaddingleft="20px"/>
    </mt-cell-group>
  </mt-tab-container-item>
</mt-tab-container>
<script>
  export default {
    data() {
      return {
        selected: '1'
      };
    },
    methods: {
      change: function(val){
        // val 为当前选中值，即v-model的value值
      }
    }
  };
</script>

```

```javascript
methods: {
  change: function(val){
    // val 为当前选中值，即v-model的value值
  }
}
```


## API

### navbar

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| fixed | 固定在页面顶部 | Boolean | | false |
| value | 返回当前选中的 tab-item 的 id | * | |  |

## Events
| 事件名称 | 说明 | 回调参数 |
|------|-------|---------|
|change | 当前选中的tab索引id | `v-model`值 |

### tab-item
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| id | 选中后的返回值 | * | |  |
| icontype | 选用的字体图标名称 | String | 参看字体图标 |  |
| badge | 可选内置徽章类型 | String | `dot` | '' |

## Slot
### navbar
| name | 描述 |
|------|--------|
| - | 内容 |

### tab-item
| name | 描述 |
|------|--------|
| - | 显示文字|
|icon | icon 图标，用于插入图片（与icontype效果相同，两者可选其一）|
|badge | badge 徽章,存在内置红点徽章(dot),也可自定义,但必要时需要对样式进行修改 |
