<template>
  <div class="section h-40 bg-light flex items-center justify-center">
    <h2 class="block text-2xl">{{ text }}</h2>
  </div>
</template>

<script>
export default {
  name: "SectionHeadline",
  props: {
    text: {
      type: String,
      default: "Ich bin eine Section Headline"
    }
  }
}
</script>
