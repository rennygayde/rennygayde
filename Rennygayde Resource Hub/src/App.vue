<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';
</script>

<template>
  <header>
    <NavBar />
  </header>
  <main>
    <div id="navbar-spacer" style="height: 30px;"></div>
    <RouterView />
    <div style="height:200vh"></div>
  </main>
</template>
