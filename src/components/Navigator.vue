<template>
    <div>
      <el-row>
        <el-col :xs="0" :sm="3" :md="3" :lg="3" class="sideCol"></el-col>
        <el-col :xs="24" :sm="18" :md="18" :lg="18" class="middle_wrapper">
            <div class="logo">
              <img src='../assets/navigator/logo-50.png' height="60px" width="60px" />
            </div>
            <div class="right_navigator">
              <el-menu :default-active="activeIndex" class="right_navigator_menu" mode="horizontal" @select="handleSelect">
                <el-menu-item index="1" class="right_navigator_menu_item">首页</el-menu-item>
                <el-submenu index="2">
                  <template slot="title">博客</template>
                  <el-menu-item index="2-1" class="right_navigator_menu_sub_items">干货</el-menu-item>
                  <el-menu-item index="2-2" class="right_navigator_menu_sub_items">杂记</el-menu-item>
                  <el-menu-item index="2-3" class="right_navigator_menu_sub_items">游记</el-menu-item>
                </el-submenu>
                <el-menu-item index="3" class="right_navigator_menu_item">关于</el-menu-item>
              </el-menu>
            </div>
        </el-col>
        <el-col :xs="0" :sm="3" :md="3" :lg="3" class="sideCol"></el-col>
      </el-row>
    </div>
</template>

<script lang="ts">
import { Button, Row, Col, Menu, MenuItem, Submenu } from 'element-ui';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'HelloWorld',
  components:{
    'el-button':Button,
    'el-row':Row,
    'el-col':Col,
    'el-menu':Menu,
    'el-menu-item':MenuItem,
    'el-submenu':Submenu,
  },
  data () {
    return {
      msg: 'hellow ts',
      activeIndex: '1',
      activeIndex2: '1'
    }
  },
  methods: {
      handleSelect(key:string, keyPath:string) {
        console.log(key, keyPath);
      }
    }
})
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .sideCol::after{
    display: inline-block;
    content: '';
    width: 100%;
    line-height: 0;
    font-size: 0;
  }
  .middle_wrapper{
    height: 60px;
    line-height: 60px;
  }
  .logo{
     float: left;
  }
  .rightNavigator {
    float: right;
  }
  .right_navigator_menu{
    height: 60px;
    display: inline-block;
    float: right;
  }
  .right_navigator_menu_item{
    height: 60px;
    line-height: 60px;
  }
  .right_navigator_menu_sub_items{
    min-width: 80px;
    width: 80px;
  }
  #iconWrap {
    overflow: visible;
  }
  
</style>
