<script setup lang="ts">
import CVHeader from './CVHeader.vue';
import CVMain from './CVMain.vue';

const title = import.meta.env.VITE_NAME ? import.meta.env.VITE_NAME : ""
const subtitle = import.meta.env.VITE_SUBTITLE ? import.meta.env.VITE_SUBTITLE : ""
</script>

<template>
  <div class="page padding-5mm">
    <CVHeader :title="title" :subtitle="subtitle" />
    <CVMain />
  </div>
</template>

<style scoped>
.header {
  color: #fff;
  background-color: #f1c042;
}

h1 {
  text-transform: uppercase;
  font-size: 2.2em;
  line-height: 1.1;
}
</style>
