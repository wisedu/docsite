# Infinite scroll

> 无限滚动指令。

-------------

## 引入

```javascript
import { InfiniteScroll } from 'bh-mint-ui2';

Vue.use(InfiniteScroll);
```

## 基本用法实例

为 HTML 元素添加 `v-infinite-scroll` 指令即可使用无限滚动。滚动该元素，当其底部与被滚动元素底部的距离小于给定的阈值（通过 `infinite-scroll-distance` 设置）时，绑定到 `v-infinite-scroll` 指令的方法就会被触发。


```html
<ul
  v-infinite-scroll="loadMore"
  infinite-scroll-disabled="loading"
  infinite-scroll-distance="40">
  <li v-for="item in list">{{ item }}</li>
</ul>
<p v-show="loading" class="page-infinite-loading">
  <mt-spinner type="fading-circle"></mt-spinner>
  加载中...
</p>
<p v-show="allLoaded" class="page-infinite-loading">没有更多数据了</p>
```

```javascript
data() {
  return {
    list: [],
    loading: false,
    allLoaded: false
  };
},
methods: {
  loadMore() {
    if(this.list.length && this.list[this.list.length - 1]>=50) {
      this.allLoaded = true;
      return
    };
    this.loading = true;
    //api数据请求
    axios.get('https://res.wisedu.com/fe_components/mock/select.json').then(resp => {
      let last = this.list.length?this.list[this.list.length - 1]:0;
      for (let i = 1; i <= 5; i++) {
        this.list.push(last + i);
      }
      this.loading = false;
    });
  }
}
```

## 与navbar组件组合使用
```html
<mt-navbar v-model="selected" @change="change">
  <mt-tab-item id="1" >选项一四</mt-tab-item>
  <mt-tab-item id="2" >选项二四</mt-tab-item>
  <mt-tab-item id="3" >选项三四</mt-tab-item>
</mt-navbar>
<mt-tab-container v-model="selected" >
  <mt-tab-container-item id="1">
    <mt-cell-group>
      <mt-cell v-for="n in 20" :key="n" :title="'内容 ' + n" wrapperpaddingleft="20px"/>
    </mt-cell-group>
  </mt-tab-container-item>
  <mt-tab-container-item id="2">
    <mt-cell-group>
      <mt-cell v-for="n in 10" :key="n" :title="'测试 ' + n" wrapperpaddingleft="20px"/>
    </mt-cell-group>
  </mt-tab-container-item>
  <mt-tab-container-item id="3">
    <div class="page-infinite-wrapper" ref="wrapper" :style="{ 'max-height': wrapperHeight + 'px' }">
      <ul class="page-infinite-list" v-infinite-scroll="loadMore" infinite-scroll-disabled="loading" infinite-scroll-distance="50" infinite-scroll-immediate-check="check">
        <li v-for="item in list" class="page-infinite-listitem">{{ item }}</li>
      </ul>
      <p v-show="loading" class="page-infinite-loading">
        <mt-spinner type="fading-circle"></mt-spinner>
        加载中...
      </p>
      <p v-show="allLoaded" class="page-infinite-loading">没有更多数据了</p>
    </div>
  </mt-tab-container-item>
</mt-tab-container>
```
```javascript
<script>
  import axios from 'axios';
  export default {
    data() {
      return {
        list: [],
        loading: false,
        allLoaded: false,
        check: false,
        wrapperHeight: 0,
        selected: '1'
      };
    },

    methods: {
      loadMore() {
        if(this.list.length && this.list[this.list.length - 1]>=50) {
          this.allLoaded = true;
          return
        };
        this.loading = true;
        axios.get('https://res.wisedu.com/fe_components/mock/select.json').then(resp => {
          let last = this.list.length?this.list[this.list.length - 1]:0;
          for (let i = 1; i <= 4; i++) {
            this.list.push(last + i);
          }
          this.loading = false;
        });
      },
      change: function(val){
        if(val === '3') {
          this.check = true;
          this.$nextTick(function(){
            this.wrapperHeight = document.documentElement.clientHeight - this.$refs.wrapper.getBoundingClientRect().top;
          })
        }
      }
    }
  };
</script>

```


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| v-infinite-scroll | 无限加载调用方法 | Funtion | - | - |
| infinite-scroll-disabled | 若为真，则无限滚动不会被触发 | Boolean | | false |
| infinite-scroll-distance | 触发加载方法的滚动距离阈值（像素） | Number | | 0 |
| infinite-scroll-immediate-check | 若为真，则指令被绑定到元素上后会立即检查是否需要执行加载方法。在初始状态下内容有可能撑不满容器时十分有用。 | Boolean | | true |
