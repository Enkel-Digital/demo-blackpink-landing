<template>
  <!-- <div class="is-pulled-right" id="albums"> -->
  <div id="albums">
    <div v-for="(album, i) in albums" :key="i">
      <img
        :src="require(`../assets/albums/${album.image}`)"
        :alt="album.name"
        class="image album-image"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Albums",
  data() {
    return {
      albums: [
        {
          image: "square up.gif",
          name: "Square Up",
        },
        {
          image: "square two.png",
          name: "Square Two",
        },
        {
          image: "square one.jpg",
          name: "Square One",
        },
      ],
    };
  },
};
</script>

<style scoped>
#albums {
  /* overflow-y: scroll; */
}

.album-image {
  width: 33vw;

  /* @todo Instead of em using % that scales for mobile view */
  margin: 6em;
}
</style>
