<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext" />
    </base-section>
    <base-section>
      <text-area :content="paragraphs[0]" />
    </base-section>
  </Layout>
</template>

<script>
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
    TextArea
  },
  data() {
    return barf
  }
}
</script>
