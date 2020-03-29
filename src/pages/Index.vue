<template>
  <Layout>
    <base-section>
      <intro-area
        :image="image"
        :is-home="true"
        :intro-text="introtext"
      ></intro-area>
    </base-section>
    <base-section>
      <info-box :content="infobox"></info-box>
    </base-section>
    <Menu />
    <base-section>
      <text-area :content="paragraphs[0]" />
    </base-section>

    <base-section>
      <parallax-image :image="'tine'"></parallax-image>
    </base-section>

    <base-section>
      <text-area :content="paragraphs[1]" />
    </base-section>

    <base-section>
      <logo-show-case></logo-show-case>
    </base-section>

    <base-section>
      <parallax-image :image="'tineRunning'"></parallax-image>
    </base-section>

    <Footer />
  </Layout>
</template>

<script>
import home from "../data/home.json"
import IntroArea from "../components/IntroArea"
import BaseSection from "../components/BaseSection"
import InfoBox from "../components/InfoBox"
import TextArea from "../components/TextArea"
import Footer from "../components/Footer"
import ParallaxImage from "../components/ParallaxImage"
import LogoShowCase from "../components/LogoShowCase"
import Menu from "../components/Menu"

export default {
  components: {
    BaseSection,
    IntroArea,
    InfoBox,
    TextArea,
    Footer,
    ParallaxImage,
    LogoShowCase,
    Menu
  },
  data() {
    return home
  },
  metaInfo: {
    title: "Kooikerhondjes von der Wiesbachaue"
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
.bg-light {
  background-color: #f4d8cd;
}
</style>
