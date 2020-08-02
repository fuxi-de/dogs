<template>
  <Layout>
    <div class="min-h-screen flex-col flex justify-center py-32 bg-light">
      <text-area
        v-for="paragraph in data.paragraphs"
        :key="paragraph.index"
        :headline="paragraph.headline"
        :content="paragraph.content"
      />
    </div>
  </Layout>
</template>

<script>
import TextArea from "../components/TextArea"
import impressum from "../data/impressum.json"

export default {
  metaInfo: {
    title: "Impressum"
  },
  components: {
    TextArea
  },
  data() {
    return {
      data: impressum
    }
  }
}
</script>
