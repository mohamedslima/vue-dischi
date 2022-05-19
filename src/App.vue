<template>
  <div id="app">
    <SpotifyHeader />
  </div>
</template>

<script>
import SpotifyHeader from "./components/SpotifyHeader.vue";

export default {
  name: "App",
  components: {
    SpotifyHeader,
  },
};
</script>

<style lang="scss">
@import "../node_modules//bootstrap/scss/bootstrap.scss";
</style>
