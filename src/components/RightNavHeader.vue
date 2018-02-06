<template>
    <div class="container">
        <div class="header">
            <div class="nav_title">
                <i class="el-icon-share"></i>{navTitle}
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { Button, Select, Container, Header, Main } from 'element-ui';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'RightNavHeader',
  props:['navTitle'],
  components:{

  },
  data () {
    return {
    }
  }
})
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  margin-bottom: 8px;
  padding-bottom: 5px;
  border-bottom: 2px solid #808080;;

}

.nav_title {
  font-size: 23px;
  font-weight: bold;
}
</style>
