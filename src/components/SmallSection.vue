<template>
  <div class="section w-full pb-40 bg-light" :class="pt ? 'pt-40' : ''">
    <slot />
  </div>
</template>

<script>
export default {
  name: "SmallSection",
  props: {
    pt: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style scoped lang="scss">
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 100% 25%;
}
</style>
