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
          <slide>
            <g-image
              class="mx-auto"
              src="~/assets/images/carousel/DSC_0463.jpg"
              width="800"
            />
          </slide>
          <slide>
            <g-image
              class="mx-auto"
              src="~/assets/images/carousel/_MG_9256.jpg"
              width="800"
            />
          </slide>
          <slide>
            <g-image
              class="mx-auto"
              src="~/assets/images/carousel/DSC_0458.jpg"
              width="800"
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
