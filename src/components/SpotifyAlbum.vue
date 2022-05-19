<template>
  <div>
    <SpotifyAlbumCard />
  </div>
</template>

<script>
import SpotifyAlbumCard from "./SpotifyAlbumCard.vue";
import axios from "axios";

export default {
  name: "SpotifyAlbum",
  components: {
    SpotifyAlbumCard,
  },
  data: function () {
    return {
      album: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.album = resp.data.response;
      });
  },
};
</script>

<style></style>
