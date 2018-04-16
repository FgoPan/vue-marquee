<template>
  <div class="out-box">
    <vueMarquee :data="msg" :style-object="styleObject"/>
  </div>
</template>
<script>
import vueMarquee from './components/vue-marquee'

export default {
  name: 'App',
  components: {
    vueMarquee
  },
  data() {
    return {
      msg: '谁在乎我的心里有多苦，谁在意我的明天去何处，这条路究竟多少崎岖多少坎坷途，我和你早以没有回头路',
      styleObject: {
        color: 'red',
        fontSize: '13px'
      }
    }
  }
}

</script>
<style>
.out-box {
  width: 300px;
  margin: 0 auto;
  border: 1px solid #ff6700;
}

</style>
