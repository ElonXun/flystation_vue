<template>
    <div>
      <el-row>
        <el-col :xs="0" :sm="3" :md="3" :lg="3" class="sideCol"></el-col>
        <el-col :xs="24" :sm="18" :md="18" :lg="18">
            <div class="logo">
              <img src='../assets/navigator/logo-50.png' height="50px" width="50px" />
            </div>
        </el-col>
        <el-col :xs="0" :sm="3" :md="3" :lg="3" class="sideCol"></el-col>
      </el-row>
    </div>
</template>

<script lang="ts">
import { Button, Row, Col } from 'element-ui';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'HelloWorld',
  components:{
    'el-button':Button,
    'el-row':Row,
    'el-col':Col,
  },
  data () {
    return {
      msg: 'hellow ts'
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
  .logo{
     float: left;
  }
  .rightNavigator {
    float: right;
  }
  #iconWrap {
    overflow: visible;
  }
</style>
