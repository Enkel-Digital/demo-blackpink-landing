<template>
  <!-- Hero content: will be in the middle -->
  <div class="hero-body">
    <div class="container has-text-left">
      <p class="title artist-name">BLACKPINK</p>
      <div class="icons">
        <a
          class="mx-3"
          href="https://www.instagram.com/blackpinkofficial/"
          target="_blank"
        >
          <i class="fab fa-2x fa-instagram" />
        </a>
        <a
          class="mx-3"
          href="https://twitter.com/ygofficialblink"
          target="_blank"
        >
          <i class="fab fa-2x fa-twitter" />
        </a>
        <a
          class="mx-3"
          href="https://open.spotify.com/artist/41MozSoPIsD1dJM0CLPjZF"
          target="_blank"
        >
          <i class="fab fa-2x fa-spotify" />
        </a>
        <a
          class="mx-3"
          href="https://music.apple.com/us/artist/blackpink/1141774019"
          target="_blank"
        >
          <i class="fas fa-2x fa-music" />
        </a>
        <a
          class="mx-3"
          href="https://www.youtube.com/channel/UCOmHUn--16B90oW2L6FRR3A"
          target="_blank"
        >
          <i class="fab fa-2x fa-youtube" />
        </a>
      </div>
    </div>

    <Albums id="albums" />
  </div>
</template>

<script>
import Albums from "@/components/Albums";

export default {
  name: "HeroBody",
  components: { Albums },
};
</script>

<style scoped>
.artist-name {
  color: white;
}

/* Maintain the same color regardless of clicking it */
.icons > a,
a:visited {
  color: white;
}
</style>
