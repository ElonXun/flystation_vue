<template>
    <el-container>
        <el-header height='60px'>
            <Navigator></Navigator>
        </el-header>
        <el-main>
            <el-row>
                <el-col :xs="0" :sm="3" :md="3" :lg="3">&nbsp;</el-col>
                <el-col :xs="24" :sm="18" :md="18" :lg="18">
                    <el-row :gutter="16" style="margin-left: -8px; margin-right: -8px;">
                        <el-col :span="16">
                            <ArticleSelect/>   
                        </el-col>
                        <el-col :span="8">
                            <div class="right_nav">
                                <div class="right_nav_container">
                                    <RightNavHeader :navTitle="阅读最多" />
                                </div>
                                <div class="right_nav_container">
                                    <RightNavHeader :navTitle="标签" />
                                    <div class="tags_container">
                                    </div>
                                </div>
                            </div> 
                        </el-col>
                    </el-row>
                </el-col>
                <el-col :xs="0" :sm="3" :md="3" :lg="3">&nbsp;</el-col>
            </el-row>
        </el-main>
    </el-container>
</template>

<script lang="ts">
import { Button, Select, Container, Header, Main, Row, Col, } from 'element-ui';
import Navigator from '../components/Navigator.vue';
import ArticleSelect from '../components/ArticleSelect.vue';
import RightNavHeader from '../components/RightNavHeader.vue';
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
    'RightNavHeader':RightNavHeader,
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
    .right_nav_container {
        -webkit-box-shadow: 0px 1px 1px 1px rgba(0, 0, 0, .2);
        border-radius: 2px;
        background-color: white;
        overflow: hidden;
        padding: 8px 16px 16px;
        margin-bottom: 16px;
        min-width: 348px;
    }

    .most_read_content {
        font-size: 14px;
        font-weight: 500;
        margin-bottom: 10px;
    }

    .tags_container {
        /*margin-bottom: 10px;*/
    }

    .tag_wrap {
        margin-bottom: 8px;
        -webkit-box-shadow: 0px 1px 1px 1px rgba(0, 0, 0, .2);
    }
</style>
