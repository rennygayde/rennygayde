<script setup lang="ts">
const props = defineProps(['navBarState'])
</script>

<template>
  <svg fill="currentColor" width="40px" height="40px" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
    :style="{ transform: `rotate(${props.navBarState ? 180 : 0}deg)`, transition: 'transform 0.3s ease' }">
    <g id="SVGRepo_iconCarrier">
      <path d="M21,21H3L12,3Z"></path>
    </g>
  </svg>
</template>
