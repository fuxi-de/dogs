<template>
  <div class="h-full bg-light flex items-center">
    <div class="mx-auto md:w-2/3 w-4/5">
      <h2
        v-if="headline"
        class="block text-3xl text-center mb-16 font-semibold"
      >
        {{ headline }}
      </h2>
      <p
        :class="centered ? 'md:text-center' : 'md:text-left'"
        class="block mb-8 text-xl leading-loose font-light text-justify"
      >
        {{ content }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "TextArea",
  props: {
    content: {
      type: String,
      default: "content"
    },
    headline: {
      type: String,
      default: ""
    },
    centered: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss">
.bg-light {
  background-color: #f4d8cd;
  color: #011627;
}
.bg-dark {
  background-color: #011627;
}
h2 {
  font-family: "Work Sans", sans-serif;
}
</style>
