<template>
  <div class="section w-full h-40">
    <slot />
  </div>
</template>

<script>
export default {
  name: "SmallSection"
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
