<template>
  <div class="container">
    <Header :title="msg" @toggle-status="toggleStatus" :setStatus="officeIsBusy || setStatus"/>
    <div class="container-inner">
    </div>

    <div class="gif-container">
      <img :src="officeIsBusy || setStatus ? busy_gif : available_gif" class="gif">
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
      busy_gif:'https://media0.giphy.com/media/fQZX2aoRC1Tqw/giphy-downsized.gif',
      available_gif:'https://media.tenor.com/images/2dc16521f20539f559920271d3058651/tenor.gif'
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
