<template>
  <ClientOnly>
    <Slide>
      <g-link to="/Gesundheit/">Gesundheit</g-link>
      <g-link to="/Tine/">Tine</g-link>
      <g-link to="/Nika/">Nika</g-link>
      <g-link to="/Wuerfe/">Wuerfe</g-link>
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
