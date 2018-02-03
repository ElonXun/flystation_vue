<template>
     <div class="article-container">
          <div class="article-title-container">
            <div class="article-title-wrap">
              <p class="article-title">title</p>
              <p class="article-sub-title">subTitle
                <span style="margin-right:4px"/>阅读量:{article.blogReview}
              </p>
            </div>
          </div>
          <div class="article-thumbnail">
              <img src="http://flystation.image.alimmdn.com/blog/blogBackground/tencentBlog.jpg" height="125px" width="200px"/>
          </div>
        </div>
</template>

<script lang="ts">
import { Button, Select, Container, Header, Main } from 'element-ui';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'HelloWorld',
  components:{
    'el-button':Button,
    'el-header':Header,
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
.article-container {
  background-color: white;
  -webkit-box-shadow: 0px 1px 1px 1px rgba(0, 0, 0, .2);
  border-radius: 2px;
  height: 157px;
  margin-bottom: 16px;
  cursor: default;
  min-width: 713px;
}

.article-title-container {
  float: left;
  position: relative;
  height: 109px;
  margin-top: 24px;
  margin-bottom: 24px;
  margin-left: 32px;
}

.article-title-wrap {
  height: 100%;
  /*position: relative;*/
  min-width: 300px;
  max-width: 440px;
}

.article-thumbnail {
  float: right;
  -webkit-box-shadow: 0px 1px 1px 1px rgba(0, 0, 0, .2);
  border-radius: 2px;
  margin: 16px 16px 0 0;
  height: 125px;
}

.article-title {
  font-size: 30px;
  font-weight: bold;
  word-wrap: break-word;
  cursor: pointer;
  margin: 0;
}

.article-sub-title {
  font-size: 16px;
  position: absolute;
  bottom: 0px;
  margin: 0;
}
</style>
