<template>
  <div class="flex items-center bg-light h-full">
    <div class="w-2/3 mx-auto">
      <ClientOnly>
        <carousel
          ref="carousel"
          :navigation-enabled="true"
          :per-page="1"
          :loop="true"
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
        {{ currentSlide }}
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
  mounted() {
    this.$nextTick(() => {console.log(this.$refs["carousel"])})
    this.currentSlide = this.$refs["carousel"].currentPage;
  },
  data: function () {
    return {
      currentSlide: 0,
    };
  },
  watch: {
    currentSlide: function (value, old) {
      console.log(value);
    },
  },
};
</script>

<style lang="scss"></style>
