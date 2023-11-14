<template>
  <main class="cv-main">
    <CVAside :github-name="githubName" :github-url="githubUrl" :phone-number="phoneNumber" :email="email" />
    <CVContent />
  </main>
</template>

<script setup lang="ts">
import CVAside from './CVAside.vue';
import CVContent from './CVContent.vue'

const email = import.meta.env.VITE_EMAIL ? import.meta.env.VITE_EMAIL : ""
const githubName = import.meta.env.VITE_GITHUB_NAME ? import.meta.env.VITE_GITHUB_NAME : ""
const githubUrl = import.meta.env.VITE_GITHUB_URL ? import.meta.env.VITE_GITHUB_URL : ""
const phoneNumber = import.meta.env.VITE_PHONE_NUMBER ? import.meta.env.VITE_PHONE_NUMBER : ""
</script>

<style lang="scss" scoped>
.cv-main {
  padding: 1cm 1.5cm;
  display: flex;
  gap: 1.2cm;
}
</style>
