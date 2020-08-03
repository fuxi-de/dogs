<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext" />
    </base-section>
    <small-section>
      <text-area :content="paragraphs[0]" />
    </small-section>
  </Layout>
</template>

<script>
import SmallSection from "../components/SmallSection"
import BaseSection from "../components/BaseSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import barf from "../data/barf.json"

export default {
  metaInfo: {
    title: "Gesundheit"
  },
  components: {
    BaseSection,
    IntroArea,
    TextArea,
    SmallSection
  },
  data() {
    return barf
  }
}
</script>
