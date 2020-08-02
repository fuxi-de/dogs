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
    <Menu />
  </Layout>
</template>

<script>
import TextArea from "../components/TextArea"
import impressum from "../data/impressum.json"
import Menu from "../components/Menu"

export default {
  metaInfo: {
    title: "Impressum"
  },
  components: {
    TextArea,
    Menu
  },
  data() {
    return {
      data: impressum
    }
  }
}
</script>
