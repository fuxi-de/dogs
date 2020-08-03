<template>
  <div class="layout">
    <!-- <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header> -->
    <slot />
    <Menu />
    <Footer />
  </div>
</template>
<script>
import Footer from "../components/Footer"
import Menu from "../components/Menu"

export default {
  components: {
    Footer,
    Menu
  }
}
</script>
<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
@font-face {
  font-family: "Work Sans";
  src: url("../assets/fonts/Work_Sans/static/WorkSans-Regular.ttf");
  font-weight: normal;
}
</style>
