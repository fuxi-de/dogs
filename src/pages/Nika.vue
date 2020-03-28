<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext"></intro-area>
    </base-section>
    <Menu />
    <base-section>
      <text-area :content="paragraphs[0]"></text-area>
    </base-section>
  </Layout>
</template>

<script>
import Menu from "../components/Menu"
import BaseSection from "../components/BaseSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import nika from "../data/nika.json"

export default {
  metaInfo: {
    title: "Nika"
  },
  components: {
    BaseSection,
    IntroArea,
    TextArea,
    Menu
  },
  data() {
    return nika
  }
}
</script>
