<template>
  <ClientOnly>
    <Slide>
      <a id="home" href="/Gesundheit">
        <span>Gesundheit</span>
      </a>
      <a id="home" href="/Tine">
        <span>Tine</span>
      </a>
      <a id="home" href="/Nika">
        <span>Nika</span>
      </a>
      <a id="home" href="/Wuerfe">
        <span>Würfe</span>
      </a>
    </Slide>
  </ClientOnly>
</template>

<script>
export default {
  name: "Menu",
  components: {
    Slide: () =>
      import("vue-burger-menu")
        .then(m => m.Slide)
        .catch()
  }
};
</script>
