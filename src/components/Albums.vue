<template>
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
  /* css to make the component a scrollable column on the right */
  max-height: 100%;
  overflow-y: scroll;
  position: absolute;
  bottom: 0;
  right: 0;

  /* Give the top of the albums component a spacing that can be scrolled into */
  padding-top: 40vh;
}

.album-image {
  /* Enforce a consistent width and size since they are all squares. */
  width: 33vw;

  /* @todo Instead of em using % that scales for mobile view */
  margin: 6em;
}

/* Mobile view to move the description box up */
@media (max-width: 768px) {
  .album-image {
    /* Enforce a consistent width and size since they are all squares. */
    width: 78vw;

    /* @todo Instead of em using % that scales for mobile view */
    margin: 6em;
  }

  #albums {
    /* @todo Make the album art centered */
  }
}
</style>
