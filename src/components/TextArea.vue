<template>
  <div class="h-full bg-dark flex items-center">
    <div class="mx-auto w-2/3">
      <p class="block mb-8">
        {{ content }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TextArea',
  props: ['content'],
}
</script>

<style lang="scss">
.bg-dark {
  background-color: #011627;
  color: #f4d8cd;
}
</style>
