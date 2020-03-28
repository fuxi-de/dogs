<template>
  <ClientOnly>
    <Slide>
      <g-link to="/gesundheit/">Gesundheit</g-link>
      <g-link to="/tine/">Tine</g-link>
      <g-link to="/nika/">Nika</g-link>
      <g-link to="/wuerfe/">Wuerfe</g-link>
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
