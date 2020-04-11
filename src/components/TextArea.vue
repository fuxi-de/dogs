<template>
  <div class="h-full bg-light flex items-center">
    <div class="mx-auto w-2/3">
      <p class="block mb-8 text-xl leading-relaxed">
        {{ content }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TextArea',
  props: ['content']
}
</script>

<style lang="scss">
.bg-light {
  background-color: #f4d8cd;
  color: #011627;
}
.bg-dark{
  background-color: #011627;
}
</style>
