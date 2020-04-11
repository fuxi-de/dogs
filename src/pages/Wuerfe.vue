<template>
  <Layout>
    <base-section>
      <intro-area :image="data.image" :intro-text="data.introtext"></intro-area>
    </base-section>
    <Menu />
    <base-section>
      <VueSlickCarousel
        :arrows="true"
        :dots="true"
        @afterChange="handleAfterChange(slideIndex)"
      >
        <div>
          <g-image
            class="mx-auto"
            src="~/assets/images/carousel/_MG_9256.jpg"
            width="800"
          />
        </div>
        <div>
          <g-image
            class="mx-auto"
            src="~/assets/images/carousel/DSC_0458.jpg"
            width="800"
          />
        </div>
        <div>
          <g-image
            class="mx-auto"
            src="~/assets/images/carousel/DSC_0463.jpg"
            width="800"
          />
        </div>
      </VueSlickCarousel>
      <h1>{{slideIndex}}</h1>
    </base-section>
    <small-section>
      <text-area :content="currentThrow" />
    </small-section>
  </Layout>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel"
import Menu from "../components/Menu"
import BaseSection from "../components/BaseSection"
import SmallSection from "../components/SmallSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import throws from "../data/throws.json"

import "vue-slick-carousel/dist/vue-slick-carousel.css"

export default {
  metaInfo: {
    title: "Würfe"
  },
  components: {
    BaseSection,
    SmallSection,
    IntroArea,
    TextArea,
    VueSlickCarousel,
    Menu
  },
  data () {
    return {
      slideIndex: 0,
      data: throws
    }
  },
  computed: {
    currentThrow() {
      return this.data.paragraphs[this.slideIndex]
    }
  },
  methods: {
    handleAfterChange(slideIndex) {
      const sliderLength = 2
      this.slideIndex = slideIndex < sliderLength ? slideIndex + 1 : 0
    }
  }
}
</script>
<style lang="scss">
.bordered {
  border: 3px solid #011627;
}
</style>
