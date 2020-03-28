<template>
  <Layout>
    <base-section>
      <intro-area :image="image" :introText="introtext"></intro-area>
    </base-section>
    <base-section>
      <text-area :content="paragraphs[0]"></text-area>
    </base-section>
  </Layout>
</template>

<script>
import BaseSection from '../components/BaseSection.vue'
import IntroArea from '../components/IntroArea.vue'
import TextArea from '../components/TextArea.vue'
import tine from '../data/tine.json'

export default {
  metaInfo: {
    title: 'Tine',
  },
  components: {
    BaseSection,
    IntroArea,
    TextArea,
  },
  data() {
    return tine
  },
}
</script>
