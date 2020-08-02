<template>
  <div class="flex items-center bg-light h-full">
    <div class="w-2/3 mx-auto">
      <ClientOnly>
        <carousel
          :navigation-enabled="true"
          :per-page="1"
          :loop="true"
          @page-change="handlePageChange"
        >
          <slide v-for="(image, index) in images" :key="index"> 
            <g-image
              class="mx-auto"
              :src="image"
              width="700"
            />
          </slide>
        </carousel>
      </ClientOnly>
    </div>
  </div>
</template>

<script>
export default {
  name: "ImageSlider",
  props:{
    'images': Array
  },
  components: {
    Carousel: () =>
      import("vue-carousel")
        .then((m) => m.Carousel)
        .catch(),
    Slide: () =>
      import("vue-carousel")
        .then((m) => m.Slide)
        .catch(),
  },
  methods: {
    handlePageChange(currentPage) {
      this.$emit('propagateCurrentSlide', currentPage)
    }
  }
};
</script>

<style lang="scss"></style>
