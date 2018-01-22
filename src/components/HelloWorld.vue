<template>
  <div class="hello">
    <el-button>anniu</el-button>
     <el-container>
          <el-header>header</el-header>
          <el-main>main</el-main>
      </el-container>
  </div>
</template>

<script lang="ts">
import { Button, Select, Container, Header, Main } from 'element-ui';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'HelloWorld',
  components:{
    'el-button':Button,
    'el-container':Container,
     'el-header':Header,
     'el-main':Main,
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

</style>
