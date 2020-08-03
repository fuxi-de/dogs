<template>
  <Layout>
    <base-section>
      <intro-area :image="data.image" :intro-text="data.introtext"></intro-area>
    </base-section>
    <small-section>
      <image-slider :images="images" @propagateCurrentSlide="handleSlideChange" />
    </small-section>
    <small-section :pt="false">
      <text-area :content="currentThrow" />
    </small-section>
  </Layout>
</template>

<script>
import BaseSection from "../components/BaseSection"
import SmallSection from "../components/SmallSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import ImageSlider from "../components/ImageSlider"
import throws from "../data/throws.json"

export default {
  metaInfo: {
    title: "Würfe"
  },
  components: {
    BaseSection,
    SmallSection,
    IntroArea,
    TextArea,
    ImageSlider
  },
  data() {
    return {
      currentSlide: 0,
      data: throws,
      images: throws.throws.map(({ image }) => image)
    }
  },
  computed: {
    currentThrow() {
      return this.data.throws[this.currentSlide].text
    }
  },
  methods: {
    handleSlideChange(value) {
      this.currentSlide = value
    }
  }
}
</script>
<style lang="scss">
.bordered {
  border: 3px solid #011627;
}
</style>
