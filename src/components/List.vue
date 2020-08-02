<template>
  <div class="bg-light flex items-center mt-8">
    <div class="mx-auto w-2/3">
      <ul class="mx-auto">
        <li v-for="item in listItems" :key="item.index" class="underline text-center mb-8 text-xl leading-loose font-light">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "List",
  props: {
    listItems: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style lang="scss" scoped></style>
