<template>
  <main>
    <div>
      <SpotifySelectAlbum @insertSelected="optionSelected($event)" />
    </div>
    <div class="container_bg_card row row-cols-5">
      <SpotifyAlbumCard
        v-for="item in albumFiltered"
        :key="item"
        :album="item"
      />
    </div>
  </main>
</template>

<script>
import SpotifyAlbumCard from "./SpotifyAlbumCard.vue";
import axios from "axios";
import SpotifySelectAlbum from "./SpotifySelectAlbum.vue";

export default {
  name: "SpotifyAlbum",
  components: {
    SpotifyAlbumCard,
    SpotifySelectAlbum,
  },
  data: function () {
    return {
      album: [],
      genre: "",
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.album = resp.data.response;
      });
  },
  computed: {
    albumFiltered() {
      const filteredArray = this.album.filter((element) => {
        return element.genre.includes(this.genre);
      });
      return filteredArray;
    },
  },
  methods: {
    optionSelected(event) {
      this.genre = event;
    },
  },
};
</script>

<style lang="scss" scoped>
div.container_bg_card {
  background-color: #1e2e3c;
}
</style>
