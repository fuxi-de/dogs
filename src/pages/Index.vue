<template>
  <Layout>
    <base-section>
      <intro-area
        :image="image"
        :isHome="true"
        :introText="introtext"
      ></intro-area>
    </base-section>
    <base-section>
      <info-box :content="infobox"></info-box>
    </base-section>
    <Menu />
    <base-section>
      <text-area :content="paragraphs[0]"></text-area>
    </base-section>

    <base-section>
      <parallax-image :image="'tine'"></parallax-image>
    </base-section>

    <base-section>
      <text-area :content="paragraphs[1]"></text-area>
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
import home from '../data/home.json';
import IntroArea from '../components/IntroArea.vue';
import BaseSection from '../components/BaseSection.vue';
import InfoBox from '../components/InfoBox.vue';
import TextArea from '../components/TextArea.vue';
import Footer from '../components/Footer.vue';
import ParallaxImage from '../components/ParallaxImage.vue';
import LogoShowCase from '../components/LogoShowCase.vue';
import Menu from '../components/Menu.vue';

export default {
  data() {
    return home
  },
  metaInfo: {
    title: 'Kooikerhondjes von der Wiesbachaue',
  },
  components: {
    BaseSection,
    IntroArea,
    InfoBox,
    TextArea,
    Footer,
    ParallaxImage,
    LogoShowCase,
    Menu,
  },
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
