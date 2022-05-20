<template>
  <div class="select_bg_container">
    <div class="select_container">
      <label for="filter-genre">
        <select
          class="form-select"
          aria-label="Default select"
          @change="$emit('insertSelected', selectedGenre)"
          v-model="selectedGenre"
        >
          <option value="" selected>Tutti i generi</option>
          <option value="Pop">Pop</option>
          <option value="Rock">Rock</option>
          <option value="Metal">Jazz</option>
          <option value="Jazz">Metal</option>
        </select>
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: "SpotifySelectAlbum",
  data: function () {
    return {
      selectedGenre: "",
    };
  },
};
</script>

<style lang="scss" scoped>
div.select_bg_container {
  background-color: #2f3a46;
  div.select_container {
    width: 20%;
    select {
      margin-left: 1rem;
      background-color: #2f3a46;
      color: white;
      border: 2px solid white;
      border-radius: 50px;
    }
  }
}
</style>
