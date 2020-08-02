<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext"></intro-area>
    </base-section>
    <small-section>
      <text-area :content="paragraphs[0]"></text-area>
    </small-section>
    <!-- <base-section>
      <image-slider />
    </base-section> -->
  </Layout>
</template>

<script>
import BaseSection from "../components/BaseSection"
import SmallSection from "../components/SmallSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import nika from "../data/nika.json"

export default {
  metaInfo: {
    title: "Nika"
  },
  components: {
    BaseSection,
    SmallSection,
    IntroArea,
    TextArea
  },
  data() {
    return nika
  }
}
</script>
