<template>
  <div
    :style="{ backgroundImage: `url(${image})` }"
    class="intro bg-fixed bg-center bg-top bg-no-repeat bg-cover h-full"
  >
    <div class="layer">
      <span class="mx-auto">
        <p>{{ introText }}</p>
        <g-image
          v-if="isHome === true"
          src="~/assets/images/barf.png"
          width="150"
        />
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "IntroArea",
  props: ["isHome", "introText", "image"]
}
</script>

<style lang="scss">
.intro {
  //background-image: url("../assets/images/wiesbachaue.jpg");
  .layer {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0, 0, 0, 0.5);
    span {
      font-size: 3rem;
      width: 50%;
      display: block;
      padding-top: 13rem;
      color: #f4d8cd;
    }
  }
}
</style>
