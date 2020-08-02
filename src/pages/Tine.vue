<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext" />
    </base-section>
    <small-section>
      <text-area :content="paragraphs[0]" />
    </small-section>
    <base-section>
      <image-slider :images="images"/>
    </base-section>
  </Layout>
</template>

<script>
import BaseSection from "../components/BaseSection"
import SmallSection from "../components/SmallSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import ImageSlider from "../components/ImageSlider"
import tine from "../data/tine.json"

export default {
  metaInfo: {
    title: "Tine"
  },
  components: {
    BaseSection,
    IntroArea,
    TextArea,
    ImageSlider,
    SmallSection
  },
  data() {
    return tine
  }
}
</script>
