<template>
  <div class="container">
    <Header :title="msg" @toggle-status="toggleStatus" :setStatus="officeIsBusy || setStatus"/>
    <div class="container-inner">
    </div>

  </div>
  
</template>

<script>
import Header from '../components/Header.vue'
export default {
  name: 'Home',
  props: {
    msg: String,
    officeIsBusy: Boolean
  },
  data() {
    return {
      setStatus: false,
    }
  },
  components:{
    Header
  },
  methods: {
    toggleStatus() {
      this.setStatus = !this.setStatus
      console.log("#",this.setStatus)
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >


</style>
