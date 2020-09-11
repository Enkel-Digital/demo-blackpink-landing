<template>
  <!-- <div class="hero-body"> -->
  <div class="columns is-centered is-multiline">
    <div class="description-box-position column is-6">
      <div class="has-text-left">
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
    </div>

    <div class="column is-6">
      <Albums />
    </div>
  </div>
  <!-- </div> -->
</template>

<script>
import Albums from "@/components/Albums";

export default {
  name: "HeroBody",
  components: { Albums },
};
</script>

<style scoped>
/* Maintain the same color regardless of clicking it */
.artist-name,
.icons > a,
a:visited {
  color: white;
}

.description-box-position {
  position: absolute;
  top: 46%;
  left: 10%;
}

/* Mobile view to move the description box up */
@media (max-width: 768px) {
  .description-box-position {
    /* Move it higher to be on top of the scrolling albums */
    top: 10%;
  }
}
</style>
