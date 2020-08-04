<template>
  <ClientOnly>
    <Slide>
      <g-link to="/">Startseite</g-link>
      <g-link to="/gesundheit/">Gesundheit</g-link>
      <g-link to="/tine/">Tine</g-link>
      <g-link to="/nika/">Nika</g-link>
      <g-link to="/wuerfe/">Würfe</g-link>
      <g-link to="/impressum/">Impressum</g-link>
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
<style lang="scss">
.bm-burger-button{
  position:fixed !important;
}
.bm-burger-bars{
  background-color:#f4d8cd !important;
  outline:1px solid #011627;
}
.bm-menu{
  background:  #011627 !important;
  a{
    color: #f4d8cd;
    font-family: 'Work Sans', sans-serif;
  }
  .bm-cross{
    background:  #f4d8cd !important;
  }
}
</style>

