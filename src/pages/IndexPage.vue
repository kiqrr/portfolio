<template>
  <q-page class="flex flex-center grid-background">
    <q-separator inset />
  </q-page>
</template>

<script setup>
//
</script>

<style>
header {
  padding-inline: 20%;
}

.grid-background:before {
  background-image: url(src/assets/grid.svg);
  background-repeat: repeat;
  content: '';
  height: 100%;
  inset: 0;
  opacity: 0.2;
  pointer-events: none;
  position: absolute;
  position: fixed;
  width: 100%;
  z-index: -1;
}
</style>
