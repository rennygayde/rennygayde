<script setup lang="ts">
import { ref } from 'vue';
import { RouterLink } from 'vue-router'
import IconNavbarToggle from './icons/IconNavbarToggle.vue';

const showNavbar = ref(true)
function toggleNavbar() {
  showNavbar.value = !showNavbar.value
  // some animation and stuff
}
</script>

<template>
  <nav :style="{ transform: `translate(0px,${showNavbar ? -30 : -150}px)` }">
    <RouterLink to="/">
      <div class="option">Home</div>
    </RouterLink>
    <RouterLink to="/about">
      <div class="option">About</div>
    </RouterLink>
    <RouterLink to="/report">
      <div class="option">
        Report Rennygayde Classics
      </div>
    </RouterLink>
    <RouterLink to="/magik">
      <div class="option">
        Magik Stuff
      </div>
    </RouterLink>
    <RouterLink to="/resources">
      <div class="option">
        LGBTQIA+ Resources
      </div>
    </RouterLink>
  </nav>
  <div class="toggleWrapper">
    <IconNavbarToggle @click="toggleNavbar" :navBarState="showNavbar" />
  </div>
</template>

<style lang="css" scoped>
div.option {
  display: inline-block;
  min-width: fit-content;
  max-width: 200px;
  width: 200px;
  transition: 0.4s;
  padding: auto;
  line-height: 30px;
}

div.option:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}

nav {
  padding: auto;
  text-align: center;
  background-color: var(--color-background-soft);
  transition: transform 0.3s ease;
  position: fixed;
  max-width: 1216px;
  width: 100%;
}

div.toggleWrapper {
  position: fixed;
}
</style>
