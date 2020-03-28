<template>
  <Layout>
    <base-section>
      <intro-area></intro-area>
    </base-section>
  </Layout>
</template>

<script>

import IntroArea from '../components/IntroArea.vue'
import BaseSection from '../components/BaseSection.vue'

export default {
  metaInfo: {
    title: 'Würfe',
  },
  components: {
    BaseSection,
    IntroArea,
  },
}
</script>
