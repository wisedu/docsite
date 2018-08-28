# Dropdown menus

> 下拉菜单，支持一级菜单，二级菜单，三级菜单，筛选类型。

-------------

## 引入

```javascript
import { DropdownMenus } from 'bh-mint-ui2';

Vue.component(DropdownMenus.name, DropdownMenus);
```

## 例子

`options` 属性为组件的绑定值。
*  `label`: 按钮上显示的文字，`label` 值为一个 `string`类型
*  `value`: 按钮的id，`value` 值为一个 `string` 类型
*  `type`: 按钮的类型，`type` 值目前有四类，分别是'lv1':一级菜单，'lv2':二级菜单，'lv3':三级菜单，'filter':筛选菜单

`dropDown` 监听此event，获取到被点击的按钮参数对象

`cancel` 监听此event，当触发此事件时，需要收起下拉菜单

```html
<template>
  <mt-dropdown-menus
    :options="options"
    @dropDown="getSelectedButtons"
    @cancel="cancel">
    <div v-if="isShowMenu" slot="menu">需要展示的自定义内容1</div>
  </mt-dropdown-menus>
</template>

<script>
  export default {
    data() {
      return {
        //结合使用的数据
        isShowMenu: false,
        options:[]
      }
    }
    methods: {
      getSelectedButtons(param) {
        console.log(param)
      },
      cancel:function(){
          //隐藏下拉菜单
      }
    }
  };
</script>
```

下拉菜单允许自定义，下面展示一个实例

```html
<template>
  <div class="page-part part-height">
    <h2>一级下拉菜单</h2>
    <mt-dropdown-menus :options="options1" @dropDown="getSelectedButtons1" @cancel="cancel1">
      <mt-box-group v-if="isShowMenu1" v-model="sexValue1" align="right" slot="menu">
        <mt-cell-group>
            <mt-radiobox :name="item.value" :disabled="item.disabled" type="hook" v-for="item in menuDatas1" :key="item.value">
                {{item.label}}
            </mt-radiobox>
        </mt-cell-group>
      </mt-box-group>
    </mt-dropdown-menus>
  </div>
  <div class="page-part part-height">
    <h2>二级下拉菜单</h2>
    <mt-dropdown-menus :options="options2" @dropDown="getSelectedButtons2" @cancel="cancel2">
      <mt-side-navbar v-if="isShowMenu2" slot="menu" class="bh-ddm-sideNavbar" v-model="lv2Selected2">
        <div slot="nav">
          <mt-tab-item id="4">全部国家</mt-tab-item>
          <mt-tab-item id="1">选项一</mt-tab-item>
          <mt-tab-item id="2">选项二</mt-tab-item>
          <mt-tab-item id="3">选项三</mt-tab-item>
        </div>
        <mt-tab-container v-model="lv2Selected2" slot="content">
          <mt-tab-container-item id="4">
            <mt-cell :title="'国家'" :id="'countryAll'" arrowdefined is-link to="click" @cellClick="cellClick2">
              <i slot="arrowdefined" class="icon"></i>
            </mt-cell>
          </mt-tab-container-item>
          <mt-tab-container-item id="1">
            <mt-cell v-for="n in 10" :title="'内容 ' + n" arrowdefined :id="n" is-link to="click" @cellClick="cellClick2">
                <i slot="arrowdefined" class="icon"></i>
            </mt-cell>
          </mt-tab-container-item>
          <mt-tab-container-item id="2">
            <mt-cell v-for="n in 4" :title="'测试 ' + n" arrowdefined :aria-invalid="n" is-link to="click" @cellClick="cellClick2">
              <i slot="arrowdefined" class="icon"></i>
            </mt-cell>
          </mt-tab-container-item>
          <mt-tab-container-item id="3">
            <mt-cell v-for="n in 6" :title="'选项 ' + n" arrowdefined :id="n" is-link to="click" @cellClick="cellClick2">
                <i slot="arrowdefined" class="icon"></i>
            </mt-cell>
          </mt-tab-container-item>
        </mt-tab-container>
      </mt-side-navbar>
    </mt-dropdown-menus>
  </div>
  <div class="page-part part-height">
    <h2>三级下拉菜单</h2>
    <mt-dropdown-menus :options="options3" @dropDown="getSelectedButtons3" @cancel="cancel3">
      <div v-if="isShowMenu3" slot="menu" class="bh-ddm-three">
        <div class="bh-ddm-lv1-container">
            <mt-cell v-for=" item in menuDatas3" :title="item.label" arrowdefined is-link :to="'click'" class="bh-ddm-lv1-item" :class="{'bh-ddm-lv1-item-selected':item.active}" @cellClick="setSelected3(item)">
                <i slot="arrowdefined" class="icon"></i>
            </mt-cell>
        </div>
        <div class="bh-ddm-lv2-container">
            <mt-cell v-for=" item in subMenuDatas3" :title="item.label" arrowdefined is-link :to="'click'" class="bh-ddm-lv2-item" :class="{'bh-ddm-lv2-item-selected':item.active}" @cellClick="setSubSelected3(item)">
                <i slot="arrowdefined" class="icon"></i>
            </mt-cell>
        </div>
        <div class="bh-ddm-lv3-container">
          <mt-box-group v-model="trafficValue3" align="right" slot="menu">
            <mt-cell-group>
                <mt-radiobox :name="item.value" :disabled="item.disabled" type="hook" v-for="item in grandMenuDatas3" :key="item.value">
                    {{item.label}}
                </mt-radiobox>
            </mt-cell-group>
          </mt-box-group>
        </div>
      </div>
    </mt-dropdown-menus>
  </div>
  <div class="page-part part-height">
    <h2>下拉条件过滤</h2>
    <mt-dropdown-menus :options="options4" @dropDown="getSelectedButtons4" @cancel="cancel4">
      <div v-if="isShowMenu4" slot="menu" class="bh-ddm-filter" :style="{'height':bodyHeight1}">
        <div style="padding:0 20px;">
            <mt-button-list label="频率" :multiple="true" :plain="false" :options="filterMenuDatas4" v-model="multiValue1" :display.sync="multiValue_display1"></mt-button-list>
            <p>value: {{multiValue1}}</p>
            <p>display: {{multiValue_display1}}</p>
        </div>
        <div class="bh-ddm-filter-buttons">
            <div class="bh-ddm-filter-button" @click="resetFilter1">
            重置
            </div>
            <div class="bh-ddm-filter-button" @click="sureFilter1">
            确定
            </div>
        </div>
      </div>
    </mt-dropdown-menus>
  </div>
  <div class="page-part part-height">
      <h2>两种类型结合使用</h2>
      <mt-dropdown-menus :options="options" @dropDown="getSelectedButtons" @cancel="cancel">
        <div v-if="isShowMenu" slot="menu">
            <mt-box-group  v-if="type==='lv1'" v-model="sexValue" align="right">
              <mt-cell-group>
                  <mt-radiobox :name="item.value" :disabled="item.disabled" type="hook" v-for="item in menuDatas" :key="item.value">
                      {{item.label}}
                  </mt-radiobox>
              </mt-cell-group>
            </div>
            <div v-if="type==='filter'" class="bh-ddm-filter" :style="{'height':bodyHeight}">
                <div style="padding:0 20px;">
                    <mt-button-list label="频率" :multiple="true" :plain="false" :options="filterMenuDatas" v-model="multiValue" :display.sync="multiValue_displaymultiValue_display"></mt-button-list>
                    <p>value: {{multiValue}}</p>
                    <p>display: {{multiValue_display}}</p>
                </div>
                <div class="bh-ddm-filter-buttons">
                    <div class="bh-ddm-filter-button" @click="resetFilter">
                    重置
                    </div>
                    <div class="bh-ddm-filter-button" @click="sureFilter">
                    确定
                    </div>
                </div>
            </div>
        </div>
      </mt-dropdown-menus>
  </div>
</template>

<script>
//一级下拉菜单js(单独使用)
export default {
  name: "page-field1",
  data() {
    return {
      options1:[{
        label: "性别",
        value: "sex"
      }],
      sexValue1:[],
      isShowMenu1:false,
      menuDatas1:[{
        label: "全部",
        value: "sexAll",
        originLabel:'性别',
        originValue:'sex'
      },{
        label: "男",
        value: "man"
      },{
        label: "女",
        value: "woman"
      }]
    }
  },
  watch: {
    sexValue1: function(newData, oldData) {
      this.changeSelectValus1(newData, that.menuDatas1);
    }
  },
  created() {},
  methods: {
    cancel1:function(){
      this.isShowMenu1 = false;
    },
    getSelectedButtons1: function(item) {
      this.isShowMenu1 = true;
    },
    changeSelectValus1: function(newData, arr) {
      var that = this;
      var selectItem = {};
      that.isShowMenu1 = false;
      if (arr) {
        arr.forEach(function(item) {
          if (item.value === newData) {
            that.$set(item, "active", true);
            selectItem = item;
          } else {
            that.$set(item, "active", false);
          }
        });
      }else {
        selectItem = {
          label:newData.title,
          value:newData.id
        };
      }
      that.options1.forEach(function(ele) {
        if (ele.active) {
          ele.active = false;
          ele.label = selectItem.originLabel?selectItem.originLabel:selectItem.label;
        }
      });
    }
  }
};
//二级下拉菜单js(单独使用)
export default {
  name: "page-field2",
  data() {
    return {
      options2:[{
          label: "国家",
          value: "country"
        }],
      isShowMenu2:false,
      lv2Selected2:'',
      lv2SelectedId2:''
    };
  },
  components: {},
  mounted() {},
  watch: {
    lv2SelectedId2:function(newData, oldData){
      var that = this;
      that.changeSelectValus2(newData);
    }
  },
  created() {},
  methods: {
    cancel2:function(){
      this.isShowMenu2 = false;
    },
    getSelectedButtons2: function(item) {
      this.isShowMenu2 = true;
    },
    cellClick2:function(param,item){
      this.lv2SelectedId2 = item;
    },
    changeSelectValus2: function(newData, arr) {
      var that = this;
      var selectItem = {};
      that.isShowMenu2 = false;
      if (arr) {
        arr.forEach(function(item) {
          if (item.value === newData) {
            that.$set(item, "active", true);
            selectItem = item;
          } else {
            that.$set(item, "active", false);
          }
        });
      }else {
        selectItem = {
          label:newData.title,
          value:newData.id
        };
      }
      that.options2.forEach(function(ele) {
        if (ele.active) {
          ele.active = false;
          ele.label = selectItem.originLabel?selectItem.originLabel:selectItem.label;
        }
      });
    }
  }
};
//三级下拉菜单js(单独使用)
export default {
  name: "page-field3",
  data() {
    return {
      options3:[{
        label: "交通",
        value: "traffic"
      }],
      isShowMenu3:false,
      menuDatas3:[{
        label: "全部",
        value: "trafficAll",
        originLabel:'交通',
        originValue:'traffic'
      },{
        label: "地铁",
        value: "metro"
      },{
        label: "公交",
        value: "bus"
      }],
      subMenuDatas3:[],
      grandMenuDatas3:[],
      trafficValue3:[],
      subParent3:{},
      grandParent3:{}
    };
  },
  components: {},
  mounted() {},
  watch: {
    trafficValue3: function(newData, oldData) {
      var that = this;
      that.changeSelectValus3(newData, that.grandMenuDatas3);
    }
  },
  created() {},
  methods: {
    cancel3:function(){
      this.isShowMenu3 = false;
    },
    getSelectedButtons3: function(item) {
      this.isShowMenu3 = true;
    },
    setSelected3: function(param) {
      var that = this;
      that.$nextTick(function() {
        that.menuDatas3.forEach(function(item) {
          that.$set(item, "active", false);
        });
        that.$set(param, "active", true);
        if (param.value.indexOf("All") > -1) {
          that.subMenuDatas3 = [];
          that.grandMenuDatas3 = [];
          that.trafficValue3 = '';
          var returnData = {
            node: {
              label: param.originLabel,
              value: param.originValue
            }
          };
          that.postEventToParent3(returnData);
        } else {
          if (param.value === "metro") {
            that.subMenuDatas3 = [
              {
                label: "一号线",
                value: "yhx"
              },
              {
                label: "三号线",
                value: "shx"
              }
            ];
          }
          that.subParent3 = param;
          //清除切换一级列表导致二级数据的变化，比如，选择某一级，点击了其二级项，再切换一级，再点击此二级的项，再返回之前的某一级，发现其二级保留了之前的状态
          that.subMenuDatas3.forEach(function(item) {
            that.$set(item, "active", false);
          });
        }
      });
    },
    setSubSelected3: function(item) {
      var that = this;
      that.$nextTick(function() {
        that.subMenuDatas3.forEach(function(item) {
          that.$set(item, "active", false);
        });
        that.$set(item, "active", true);
          //设置三级列表数据来源
        if (item.value === 'yhx') {
          this.grandMenuDatas3 = [
            {
              label: "南京南",
              value: "njn"
            },
            {
              label: "河定桥",
              value: "hdq"
            }
          ];
        }else if (item.value === 'shx'){
          this.grandMenuDatas3 = [
            {
              label: "河海大学",
              value: "hhdx"
            },
            {
              label: "机场",
              value: "jc"
            }
          ];
        }
        this.grandParent3 = item;
        //清除切换二级列表导致三级数据的变化
        this.grandMenuDatas3.forEach(function(item) {
          that.$set(item, "active", false);
        });
      });
    },
    postEventToParent3: function(data) {
      var that = this;
      if (that.type != "filter") {
        that.options3.forEach(function(ele) {
          if (ele.active) {
            ele.active = false;
            ele.label = data.node.label;
          }
        });
      }
      this.isShowMenu3 = false;
    },
    changeSelectValus3: function(newData, arr) {
      var that = this;
      var selectItem = {};
      that.isShowMenu3 = false;
      if (arr) {
        arr.forEach(function(item) {
          if (item.value === newData) {
            that.$set(item, "active", true);
            selectItem = item;
          } else {
            that.$set(item, "active", false);
          }
        });
      }else {
        selectItem = {
          label:newData.title,
          value:newData.id
        };
      }
      that.options3.forEach(function(ele) {
        if (ele.active) {
          ele.active = false;
          ele.label = selectItem.originLabel?selectItem.originLabel:selectItem.label;
        }
      });
    }
  }
};
//过滤filter菜单js(单独使用)
export default {
  name: "page-field4",
  data() {
    return {
      bodyHeight1: "",
      options4:[{
        label: "过滤",
        value: "filter"
      }],
      isShowMenu4:false,
      filterMenuDatas4: [{
        name: "1次",
        id: "1time"
      },{
        name: "2次",
        id: "2time"
      },{
        name: "3次",
        id: "3time"
      },{
        name: "4次",
        id: "4time"
      },{
        name: "5次",
        id: "5time"
      },{
        name: "6次",
        id: "6time"
      }],
      multiValue1: "",
      multiValue_display1: ""
    };
  },
  components: {},
  mounted() {},
  watch: {},
  created() {
    this.bodyHeight1 = (screen.height || document.body.clientHeight) + "px";
  },
  methods: {
    resetFilter1: function() {
      this.multiValue1 = "";
      this.multiValue_display1 = "";
    },
    sureFilter1: function() {
      console.log(this.multiValue1);
    },
    cancel4:function(){
      this.isShowMenu4 = false;
    },
    getSelectedButtons4: function(item) {
      this.isShowMenu4 = true;
    }
  }
};
</script>
```


## API
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|------|-------|---------|-------|--------|
| options | 组件的初始值 | Array | 见上面文档 | [] |


## Events
| 事件名称 | 说明 | 回调参数 |
|------|-------|---------|
| dropDown | 点击按钮时的回调函数 | `目前的选择值`,`原始dom事件` |
| cancel | 点击遮罩，取消按钮时的回调函数 | `原始dom事件` |



<script>
export default {
  name: "page-field",
  data() {
    return {
      isShowMenu: false,
      options: [{
        label: "性别",
        value: "sex",
        type: "lv1"
      },{
        label: "国家国家国",
        value: "country",
        type: "lv2"
      },{
        label: "交交通交通通",
        value: "traffic",
        type: "lv3"
      },{
        label: "筛选",
        value: "filter",
        type: "filter"
      }],
      type: "",
      menuDatas: [],
      subMenuDatas: [],
      subParent: {},
      grandMenuDatas: [],
      grandParent: {},
      filterMenuDatas: [],
      multiValue: "",
      multiValue_display: "",
      menuParent: {},
      sexValue: "",
      lv2Selected:'',
      lv2SelectedId:'',
      trafficValue: "",
      bodyHeight: ""
    };
  },
  components: {},
  mounted() {},
  watch: {
    sexValue: function(newData, oldData) {
      var that = this;
      that.changeSelectValus(newData, that.menuDatas);
    },
    trafficValue: function(newData, oldData) {
      var that = this;
      that.changeSelectValus(newData, that.grandMenuDatas);
    },
    lv2SelectedId:function(newData, oldData){
      var that = this;
      that.changeSelectValus(newData);
    }
  },
  created() {
    this.bodyHeight = (screen.height || document.body.clientHeight) + "px";
  },
  methods: {
    changeSelectValus: function(newData, arr) {
      var that = this;
      var selectItem = {};
      this.isShowMenu = false;
      if (arr) {
        arr.forEach(function(item) {
          if (item.value === newData) {
            that.$set(item, "active", true);
            selectItem = item;
          } else {
            that.$set(item, "active", false);
          }
        });
      }else {
        selectItem = {
          label:newData.title,
          value:newData.id
        };
      }
      that.options.forEach(function(ele) {
        if (ele.active) {
          ele.active = false;
          ele.label = selectItem.originLabel?selectItem.originLabel:selectItem.label;
        }
      });
    },
    getSelectedButtons: function(item) {
      this.menuParent = item;
      this.type = item.type;
      this.isShowMenu = true;
      if (
        this.menuDatas[0] &&
        this.menuDatas[0].value.indexOf(item.value) > -1
      ) {
        //   与上次一样不再重置数据
      } else {
        this.subMenuDatas = [];
        this.grandMenuDatas = [];
        if (item.value === "sex") {
          this.menuDatas = [
            {
              label: "全部性别",
              value: "sexAll",
              originLabel:'性别',
              originValue:'sex'
            },
            {
              label: "男",
              value: "man"
            },
            {
              label: "女",
              value: "woman"
            }
          ];
        } 
        // else if (item.value === "country") {
        //   this.menuDatas = [
        //     {
        //       label: "全部国家",
        //       value: "countryAll",
        //       originLabel:'国家',
        //       originValue:'country'
        //     },
        //     {
        //       label: "中国",
        //       value: "China"
        //     },
        //     {
        //       label: "美国",
        //       value: "American"
        //     }
        //   ];
        // } 
        else if (item.value === "traffic") {
          this.menuDatas = [
            {
              label: "全部交通",
              value: "trafficAll",
              originLabel:'交通',
              originValue:'traffic'
            },
            {
              label: "地铁",
              value: "metro"
            }
          ];
        } else if (item.value === "filter") {
          this.filterMenuDatas = [
            {
              name: "1次",
              id: "1time"
            },
            {
              name: "2次",
              id: "2time"
            },
            {
              name: "3次",
              id: "3time"
            },
            {
              name: "4次",
              id: "4time"
            },
            {
              name: "5次",
              id: "5time"
            },
            {
              name: "6次",
              id: "6time"
            }
          ];
        }
      }
    },
    setSelected: function(param) {
      var that = this;
      that.$nextTick(function() {
        that.menuDatas.forEach(function(item) {
          that.$set(item, "active", false);
        });
        that.$set(param, "active", true);
        if (this.type != "lv1") {
          if (param.value.indexOf("All") > -1) {
            //清除二三级的选中信息
            // if (this.subMenuDatas.length > 0) {
            //   that.subMenuDatas.forEach(function(ele) {
            //     if (ele.active) {
            //       ele.active = false;
            //     }
            //   });
            // }
            // if (that.grandMenuDatas.length > 0) {
            //   that.grandMenuDatas.forEach(function(ele) {
            //     if (ele.active) {
            //       ele.active = false;
            //     }
            //   });
            // }
            that.subMenuDatas = [];
            that.grandMenuDatas = [];
            // that.countryValue = '';
            that.trafficValue = '';
            var returnData = {
              node: {
                label: param.originLabel,
                value: param.originValue
              }
            };
            that.postEventToParent(returnData);
          } else {
            //设置二级列表数据来源
            // if (param.value === "China") {
            //   that.subMenuDatas = [
            //     {
            //       label: "江苏",
            //       value: "js"
            //     },
            //     {
            //       label: "山东",
            //       value: "sd"
            //     }
            //   ];
            // } else if (param.value === "American") {
            //   that.subMenuDatas = [
            //     {
            //       label: "纽约",
            //       value: "ny"
            //     },
            //     {
            //       label: "旧金山啊",
            //       value: "jjs"
            //     }
            //   ];
            // } else 
            if (param.value === "metro") {
              that.subMenuDatas = [
                {
                  label: "一号线",
                  value: "yhx"
                },
                {
                  label: "三号线",
                  value: "shx"
                }
              ];
            }
            that.subParent = param;
            //清除切换一级列表导致二级数据的变化，比如，选择某一级，点击了其二级项，再切换一级，再点击此二级的项，再返回之前的某一级，发现其二级保留了之前的状态
            that.subMenuDatas.forEach(function(item) {
              that.$set(item, "active", false);
            });
          }
        } else {
          if (param.value.indexOf("All") > -1) {
            var returnData = {
              node: {
                label: param.originLabel,
                value: param.originValue
              }
            };
          } else {
            var returnData = {
              node: param
            };
          }
          that.postEventToParent(returnData);
        }
      });
    },
    setSubSelected: function(item) {
      var that = this;
      that.$nextTick(function() {
        that.subMenuDatas.forEach(function(item) {
          that.$set(item, "active", false);
        });
        that.$set(item, "active", true);
        if (this.type == "lv3") {
          //设置三级列表数据来源
          if (item.value === 'yhx') {
            this.grandMenuDatas = [
              {
                label: "南京南",
                value: "njn"
              },
              {
                label: "河定桥",
                value: "hdq"
              }
            ];
          }else if (item.value === 'shx'){
            this.grandMenuDatas = [
              {
                label: "河海大学",
                value: "hhdx"
              },
              {
                label: "机场",
                value: "jc"
              }
            ];
          }
          this.grandParent = item;
          //清除切换二级列表导致三级数据的变化
          this.grandMenuDatas.forEach(function(item) {
            that.$set(item, "active", false);
          });
        } else {
          var returnData = {
            node: item,
            parentNode: this.subParentOptions
          };
          this.postEventToParent(returnData);
        }
      });
    },
    postEventToParent: function(data) {
      var that = this;
      if (that.type != "filter") {
        that.options.forEach(function(ele) {
          if (ele.active) {
            ele.active = false;
            ele.label = data.node.label;
          }
        });
      }
      this.isShowMenu = false;
    },
    resetFilter: function() {
      this.multiValue = "";
      this.multiValue_display = "";
    },
    sureFilter: function() {
      console.log(this.multiValue);
    },
    cancel:function(){
        this.isShowMenu = false;
    },
    cellClick:function(param,item){
      console.log(param)
      console.log(item)
      this.lv2SelectedId = item;
    }
  }
};
</script>
