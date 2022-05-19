<template>
  <div id="app">
    <SpotifyHeader />
    <SpotifyAlbum />
  </div>
</template>

<script>
import SpotifyHeader from "./components/SpotifyHeader.vue";
import SpotifyAlbum from "./components/SpotifyAlbum.vue";

export default {
  name: "App",
  components: {
    SpotifyHeader,
    SpotifyAlbum,
  },
};
</script>

<style lang="scss">
@import "../node_modules//bootstrap/scss/bootstrap.scss";
</style>
