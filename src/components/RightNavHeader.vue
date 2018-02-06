<template>
  <div class="hello">
    <div className={styles.container}>
      <div className={styles.header}>
        <div className={styles.navTitle}>
          <Icon type={iconType} /> {navTitle}
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Button, Select, Container, Header, Main } from 'element-ui';
import Vue, {ComponentOptions} from 'vue';
export default Vue.extend({
  name: 'RightNavHeader',
  components:{

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
