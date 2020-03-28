<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext" />
    </base-section>
    <Menu />
    <base-section>
      <text-area :content="paragraphs[0]" />
    </base-section>
  </Layout>
</template>

<script>
import Menu from "../components/Menu"
import BaseSection from "../components/BaseSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import tine from "../data/tine.json"

export default {
  metaInfo: {
    title: "Tine"
  },
  components: {
    BaseSection,
    IntroArea,
    TextArea,
    Menu
  },
  data() {
    return tine
  }
}
</script>
