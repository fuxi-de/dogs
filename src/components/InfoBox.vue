<template>
  <div class="flex items-center h-full bg-light">
    <div class="infobox mx-auto w-1/2 border-solid border-2">
      <p class="block p-8">
        {{ content }}
      </p>
      <g-image
        alt="a kooikerhondje"
        src="~/assets/images/nika.jpg"
        fit="cover"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Infobox',
  props: ['content'],
}
</script>

<style lang="scss">
.infobox {
  border-color: #011627;
}
.bg-light {
  background-color: #f4d8cd;
}
</style>
