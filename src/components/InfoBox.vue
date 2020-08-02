<template>
  <div class="flex items-center h-full bg-light pt-40">
    <div class="infobox mx-auto w-1/2 border-solid border-2">
      <p class="block p-8 text-l">
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
  props: ['content']
}
</script>

<style scoped lang="scss">
.infobox {
  border-color: #011627;
}
img{
  width:100%;
}
</style>
