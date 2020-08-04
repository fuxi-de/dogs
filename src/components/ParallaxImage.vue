<template>
  <div
    class="parallax bg-scroll md:bg-fixed bg-center bg-top bg-no-repeat bg-cover h-full"
    :style="{ backgroundImage: `url(${backgroundImage})` }"
  ></div>
</template>

<script>
import tine from '../assets/images/tine.jpg'
import tineRunning from '../assets/images/tine_running.jpg'

export default {
  name: 'ParallaxImage',
  props: ['image'],
  data() {
    return {
      images: [tine, tineRunning]
    }
  },
  computed: {
    backgroundImage() {
      if (this.image === 'tine') {
        return tine
      } return tineRunning
    }
  }
}
</script>

<style lang="scss">
</style>
