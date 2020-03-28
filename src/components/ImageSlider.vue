<template>
  <div class="flex items-center bg-light h-full">
    <div class="w-2/3 mx-auto">
      <carousel :navigationEnabled="true" :perPage="1" :loop="true">
        <slide>
          <g-image class="mx-auto" src="~/assets/images/carousel/DSC_0463.jpg" width="800"/>
        </slide>
        <slide>
            <g-image class="mx-auto" src="~/assets/images/carousel/_MG_9256.jpg" width="800"/>
        </slide>
        <slide>
            <g-image class="mx-auto" src="~/assets/images/carousel/DSC_0458.jpg" width="800"/>
        </slide>
      </carousel>
    </div>
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  name: 'ImageSlider',
  components: {
    Carousel,
    Slide,
  },
}
</script>

<style lang="scss">
</style>
