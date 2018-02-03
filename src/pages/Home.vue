<template>
    <el-container>
        <el-header height='60px'>
            <Navigator></Navigator>
        </el-header>
        <el-main>
            <el-row :gutter="16" style="margin-left: -8px; margin-right: -8px;">
                <el-col :span="16">
                    <ArticleSelect/>   
                </el-col>
                <el-col :span="8">
                    right
                </el-col>
            </el-row>
        </el-main>
    </el-container>
</template>

<script lang="ts">
import { Button, Select, Container, Header, Main, Row, Col, } from 'element-ui';
import Navigator from '../components/Navigator.vue';
import ArticleSelect from '../components/ArticleSelect.vue';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'HelloWorld',
  components:{
    'el-button':Button,
    'el-container':Container,
    'el-header':Header,
    'el-main':Main,
    'el-row':Row,
    'el-col':Col,
    'Navigator':Navigator,
    'ArticleSelect':ArticleSelect,
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
    .el-header{
        padding: 0px;
        background-color: #fff;
        height: 60px;
        line-height: 60px;
    }
    .el-main{
        padding: 0px;
        margin-top: 16px;
        overflow: hidden;
    }
</style>
