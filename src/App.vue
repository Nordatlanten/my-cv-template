<script setup lang="ts">
import Page from './components/Page.vue'
</script>

<template>
  <div class="page-outer A4">
    <Page msg="Atlan Talebi" />
  </div>
</template>

<style scoped>
.A4 {
  print-color-adjust: exact;
}
</style>
