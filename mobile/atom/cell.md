# Cell

> 单元格，可用作展示列表信息、链接或者表单等。

----------


## 引入

```javascript
import { Cell } from 'bh-mint-ui2';

Vue.component(Cell.name, Cell);
```

## 例子

将mt-cell-group组件看成一个容器即可

```html
<mt-cell-group>
  <mt-cell title="标题文字"></mt-cell>
  <mt-cell title="标题文字" value="说明文字"></mt-cell>
  <mt-cell title="标题文字" to="//github.com" is-link value="带链接 github.com"></mt-cell>
  <mt-cell title="标题文字" icon="huifu" value="左侧title带 icon"></mt-cell>
  <mt-cell title="标题文字" value="左侧title图标icon 自定义图片">
    <mt-image slot="icon" src="http://res.wisedu.com/fe_components/images/errorTip/System_upgrade.png" width="24px" height="24px" smile-display="inline-block"></mt-image>
  </mt-cell>
  <mt-cell title="标题文字" value="右侧value默认图标" is-link></mt-cell>
  <mt-cell title="标题文字" is-link value="右侧value自定义图标" arrowdefined>
    <i slot="arrowdefined" class="icon iconfont icon-localgrocerystore" style="font-size:24px;color:#bdc0c5;"></i>
  </mt-cell>
  <mt-cell title="自定义左内边距30px" wrapperpaddingleft="30px" is-link></mt-cell>
  <mt-cell title="标题文字" is-link wrapperpaddingright="30px" value="自定义右内边距30px"></mt-cell>
  <mt-cell title="标题文字" is-link wrapperpaddingright="30px" value="自定义右内边距30px">
    <span style="color: green">自定义右内边距30px</span>
  </mt-cell>
  <mt-cell title="标题" label="描述信息" is-link></mt-cell>
  <mt-cell title="自定义高度60px" label="跳转到 https://bh-mint-ui2.github.io" is-link to="https://bh-mint-ui2.github.io" cellheight="60px"></mt-cell>
  <mt-cell title="readonly状态" is-link value="内容" readonly></mt-cell>
  <mt-cell title="disabled状态" is-link value="内容" disabled></mt-cell>
</mt-cell-group>
```


带自定义图标
如以上用法不能满足你的需求，可以使用对应的slot来自定义显示的内容

```html
<mt-cell-group>
  <mt-cell title="标题文字" value="左侧title图标icon 自定义图片">
    <mt-image slot="icon" src="http://res.wisedu.com/fe_components/images/errorTip/System_upgrade.png" width="24px" height="24px" smile-display="inline-block"></mt-image>
  </mt-cell>
</mt-cell-group>
```

自定义内容，监听cellClick事件

```html
<mt-cell-group>
  <mt-cell title="标题文字" is-link to="click" @cellClick="cellClick">
    <span style="color: green">这里是元素</span>
  </mt-cell>
</mt-cell-group>
```



## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| icon  |  左侧title图标   | String    |  back, more   |     |
| title | 标题 | String | | |
| to    | 跳转链接 | String | | |
| value | 内容 | * | | |
| label | 备注信息，显示在标题下方 | String | | |
| is-link | 链接，会显示箭头图标。搭配 to 属性使用 | Boolean | | |
| cellheight | 自定义cell高度 | String | | '50px' |
| wrapperpaddingleft | 自定义cell左侧内边距 | String | | '' |
| wrapperpaddingright | 自定义cell右侧内边距 | String | | '20px(右侧无图标默认值)',<br>'15px(默认右侧有图标默认值)' |
| arrowdefined | 自定义右侧图标,与slot="arrowdefined"同时使用 | Boolean | | false |
| titlepaddingtop | 自定义title上内边距 | String | | '' |
| titlepaddingbottom | 自定义title下内边距 | String | | '' |
| titlepaddingleft | 自定义title上左边距, | String | | '' |
| titlepaddingright | 自定义title右内边距 | String | | '' |
| required | 标注是否为必选项(*) | Boolean | | false |
| titlewidth | 自定义title标签所占宽度 | String | | '' |
| valueAlign | 设定value内容的对齐方式 | String | `flex-start`,`flex-end`,'center' |  |
| readonly | 只读模式 | Boolean | | false |
| disabled | 无效模式 | Boolean | | false |

## Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| cellClick  | 点击时触发，仅设置 to="click" 时才会触发 | `原始dom事件`,`组件所携带的所有属性`  |

## Slot
| name | 描述 |
|------|--------|
| - | 自定义显示内容 |
| title | 自定义标题 |
| icon | 自定义左侧title图标 |
| arrowdefined | 自定义右侧title图标，与arrowdefined属性同时使用 |
