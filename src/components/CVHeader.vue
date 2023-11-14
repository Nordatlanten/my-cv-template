<template>
  <section class="cv-header">
    <h1 class="cv-header__title">{{ title ? title : "Firstname Lastname" }}</h1>
    <p class="cv-header__subtitle">{{ subtitle ? subtitle : "Subtitle . . ." }}</p>
  </section>
</template>

<script setup lang="ts">
defineProps<{ title: string, subtitle: string }>()
</script>

<style lang="scss" scoped>
.cv-header {
  padding-top: 2rem;
  text-align: center;
  background-color: #f1c042;
  text-transform: uppercase;

  &__title {
    color: #fff;
    font-family: Lovelo Black, sans-serif;
    font-size: 3.5rem;
    margin-bottom: 0;
  }

  &__subtitle {
    font-size: 1.2rem;
    color: #fff;
    padding-bottom: 1cm;
    margin: 2mm 0 0;
    letter-spacing: 0.2mm;
  }
}
</style>
