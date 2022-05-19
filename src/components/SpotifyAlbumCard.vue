<template>
  <div class="container_album_card mt-5">
    <div class="poster_container">
      <img :src="album.poster" alt="poster album" />
    </div>
    <h2 class="mt-2">{{ album.title }}</h2>
    <p>{{ album.author }}</p>
    <p>{{ album.year }}</p>
  </div>
</template>

<script>
export default {
  name: "SpotifyAlbumCard",
  props: {
    album: Object,
  },
};
</script>

<style lang="scss" scoped>
div.container_album_card {
  color: white;
  text-align: center;
  div.poster_container {
    img {
      width: 200px;
      height: 200px;
    }
  }
  h2 {
    font-size: 1.2rem;
    font-weight: 800;
  }
  p {
    color: #646465;
  }
}
</style>
