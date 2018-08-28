# Side Navbar

> 侧边导航

-------------

## 引入

```javascript
import { SideNavbar } from 'bh-mint-ui2';

Vue.component(SideNavbar.name, SideNavbar);
```

## 例子

`fixed` 属性为是否为绝对定位侧边导航,值为Boolean类型。

`top` 属性为侧边导航距离顶部的位置。

`width` 属性为侧边导航的宽度。


```html
<mt-side-navbar v-model="selected"> 
  <div slot="nav">
    <mt-tab-item id="1" >选项一</mt-tab-item>
    <mt-tab-item id="2" >选项二</mt-tab-item>
    <mt-tab-item id="3" >选项三</mt-tab-item>
  </div>
  <mt-tab-container v-model="selected" slot="content">
    <mt-tab-container-item id="1">
      <mt-cell-group>
        <mt-cell v-for="n in 40" :title="'内容 ' + n" cellheight="44px"/>
      </mt-cell-group>
    </mt-tab-container-item>
    <mt-tab-container-item id="2">
      <mt-cell-group>
        <mt-cell v-for="n in 4" :title="'测试 ' + n" cellheight="44px"/>
      </mt-cell-group>
    </mt-tab-container-item>
    <mt-tab-container-item id="3">
      <mt-cell-group>
        <mt-cell v-for="n in 6" :title="'选项 ' + n" cellheight="44px"/>
      </mt-cell-group>
    </mt-tab-container-item>
  </mt-tab-container>
</mt-side-navbar>
```


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| fixed | 侧边导航是否绝对定位 | Boolean | | '' |
| value | 返回当前选中的 tab-item 的 id | * | |  |
| top | 侧边导航距离顶部位置 | String | | '' |
| width | 侧边导航的宽度 | String | | '' |
| height | 导航标签的高度 | String | | '0' |

### tab-item
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| id | 选中后的返回值 | * | |  |
| icontype | 选用的字体图标名称 | String | 参看字体图标 |  |


```javascript
<script>
  export default {
    data: function(){
      return {
        selected:"1"
      }
    },
    methods:{
    }
  };
</script>
```
