<template>
  <Layout>
    <base-section>
      <intro-area
        :image="image"
        :is-home="true"
        :intro-text="introtext"
      ></intro-area>
    </base-section>

    <small-section>
      <text-area
        headline="Wir freuen uns bekannt geben zu können:"
        :content="news"
        :centered="true"
      />
      <g-image class="news__image" src="~/assets/images/dwurf.jpg" />
    </small-section>

    <small-section>
      <text-area
        headline="Bewerbungsstatus für den nächsten Wurf:"
        :content="status"
        :centered="true"
      />
    </small-section>

    <small-section>
      <text-area :headline="infobox.headline" :content="infobox.content[0]" />
      <list class="w-full md:w-2/3 mx-auto" :list-items="infobox.list" />
      <text-area :content="infobox.content[1]" />
    </small-section>

    <small-section>
      <text-area headline="Unsere Zuchtstätte" :content="paragraphs[0]" />
    </small-section>

    <base-section>
      <parallax-image :image="'tine'"></parallax-image>
    </base-section>

    <small-section>
      <text-area headline="Ein Kooikerhondje!" :content="paragraphs[1]" />
    </small-section>

    <small-section :pt="false">
      <logo-show-case></logo-show-case>
    </small-section>

    <base-section>
      <parallax-image :image="'tineRunning'"></parallax-image>
    </base-section>

    <small-section>
      <text-area
        headline="Die Frage nach dem Preis?!"
        :content="paragraphs[2].text"
      />
      <list :list-items="paragraphs[2].list" />
    </small-section>

    <small-section :pt="false">
      <text-area :content="paragraphs[3].text" />
      <list :list-items="paragraphs[3].list" />
    </small-section>

    <small-section :pt="false">
      <text-area :content="paragraphs[4]" />
      <text-area :content="paragraphs[5]" />
    </small-section>
  </Layout>
</template>

<script>
import home from "../data/home.json"
import IntroArea from "../components/IntroArea"
import BaseSection from "../components/BaseSection"
import InfoBox from "../components/InfoBox"
import TextArea from "../components/TextArea"
import ParallaxImage from "../components/ParallaxImage"
import LogoShowCase from "../components/LogoShowCase"
import SmallSection from "../components/SmallSection"
import List from "../components/List"

export default {
  components: {
    BaseSection,
    IntroArea,
    InfoBox,
    TextArea,
    ParallaxImage,
    LogoShowCase,
    SmallSection,
    List
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
.news__image{
  width: 50% !important;
  margin:auto;
  border-radius: 2%;
  border:2px solid white;
}
</style>
