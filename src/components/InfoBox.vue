<template>
  <div class="flex items-center h-full bg-light">
    <div class="infobox mx-auto w-4/5 border-solid border-2">
      <p class="block p-8 text-lg leading-loose font-light">
        {{ content.content[0] }}
      </p>
      <list :list-items="content.list" />
      <p class="block p-8 text-lg leading-loose font-light">
        {{ content.content[1] }}
      </p>
    </div>
  </div>
</template>

<script>
import List from "./List"

export default {
  name: "Infobox",
  components: {
    List
  },
  props: ["content"]
}
</script>

<style scoped lang="scss">
.infobox {
  border-color: #011627;
}
img {
  width: 100%;
}
</style>
