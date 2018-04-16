<template>
  <div class="box">
    <p class="animate" :style="styleObject">
      {{data}}
    </p>
  </div>
</template>
<script>
export default {
  name: 'marquee',
  props: {
    data: {
      required: true,
      type: String,
      default: ''
    },
    styleObject: {
      type: Object,
      default:{}
    }
  }
}

</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.box {
  width: 100%;
  position: relative;
  overflow: hidden;
}
.animate {
  padding-left: 20px;
  font-size: 12px;
  color: #000;
  display: inline-block;
  white-space: nowrap;
  animation: 15s Loop linear infinite normal;
}

@keyframes Loop {
  0% {
    transform: translateX(0px);
    -webkit-transform: translateX(0px);
  }
  100% {
    transform: translateX(-100%);
    -webkit-transform: translateX(-100%);
  }
}

@-webkit-keyframes Loop {
  0% {
    transform: translateX(0px);
    -webkit-transform: translateX(0px);
  }
  100% {
    transform: translateX(-100%);
    -webkit-transform: translateX(-100%);
  }
}

</style>
