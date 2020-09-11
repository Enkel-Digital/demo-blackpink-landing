<template>
  <div id="app">
    <section class="hero is-fullheight">
      <HeroHead />
      <!-- @todo Make the image changing -->
      <!-- <img src="./assets/hero 1.webp" alt="Hero" class="image hero-image" /> -->
      <img src="./assets/hero 2.jpg" alt="Hero" class="image hero-image" />
      <!-- <img src="./assets/hero 3.jpg" alt="Hero" class="image hero-image" /> -->
      <HeroBody />
    </section>
  </div>
</template>

<script>
import HeroHead from "@/components/HeroHead";
import HeroBody from "@/components/HeroBody";

export default {
  name: "App",
  components: {
    HeroHead,
    HeroBody,
  },
};
</script>

// Load the bulma styles in the top level component
<style lang="sass" src="bulma" />

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.hero-image {
  overflow: hidden;
  position: absolute;
  object-fit: cover;
  object-position: center center;
  width: 100%;
  height: 100%;
}
</style>
