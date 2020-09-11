<template>
  <!-- Hero head: will stick at the top on load -->
  <div class="hero-head">
    <!-- is fixed top will keep it sticky at the top of the page -->
    <nav id="nav" class="navbar is-fixed-top is-white" role="navigation">
      <!-- Container to force nav bar into center with wider side margins -->
      <div class="container">
        <div class="navbar-brand">
          <!-- <a
            href="#"
            target="_blank"
            class="navbar-item"
            style="pointer-events: none; cursor: default"
          > -->
          <!-- Use div instead of anchor tag if no links specified -->
          <div class="navbar-item">
            <img src="../assets/logo.png" alt="Logo" />
          </div>
          <!-- </a> -->

          <!-- Using <a> instead of button as it does not need an icon and dont have the inverted colors on click behaviour -->
          <a
            role="button"
            class="navbar-burger"
            :class="{ 'is-active': showMobileMenu }"
            aria-label="menu"
            data-target="navbar-menu"
            @click="showMobileMenu = !showMobileMenu"
          >
            <!-- 3 empty span tags to show the burger menu icon -->
            <span></span>
            <span></span>
            <span></span>
          </a>
        </div>

        <div
          class="navbar-menu has-text-right"
          :class="{ 'is-active': showMobileMenu }"
        >
          <!-- Show the menu at the other end -->
          <div class="navbar-end" @click="showMobileMenu = false">
            <!-- <a class="navbar-item">Home</a> -->
            <!-- <a class="navbar-item">About</a> -->

            <a
              href="https://solutions.enkeldigital.com/"
              target="_blank"
              class="navbar-item"
            >
              <img src="../assets/ekd_logo.png" alt="Enkel Digital's Logo" />
            </a>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "HeroHead",
  data() {
    return {
      showMobileMenu: false,
    };
  },
};
</script>
