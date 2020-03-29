<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :intro-text="introtext"></intro-area>
    </base-section>
    <Menu />
    <base-section>
      <div class="dark pt-8">
        <g-image
          alt="a kooikerhondje"
          src="~/assets/images/awurf.jpg"
          fit="cover"
        />
      </div>
      <text-area :content="paragraphs[0]"></text-area>
    </base-section>
  </Layout>
</template>

<script>
import Menu from "../components/Menu"
import BaseSection from "../components/BaseSection"
import IntroArea from "../components/IntroArea"
import TextArea from "../components/TextArea"
import throws from "../data/throws.json"

export default {
  metaInfo: {
    title: "Würfe"
  },
  components: {
    BaseSection,
    IntroArea,
    TextArea,
    Menu
  },
  data() {
    return throws
  }
}
</script>
<style lang="scss">
.dark {
  background-color: #011627;
  img{
    margin:auto;
  }
}
</style>
