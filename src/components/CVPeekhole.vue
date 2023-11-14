<template>
  <div class="cv-peekhole">
    <img src="../assets/selfie.jpg" alt="My lorem selfie!">
    <span>I look forward to lorem ipsum with you!</span>
    <small>Fun fact: I made this lorem ipsum with just (S)CSS.</small>
  </div>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>
.cv-peekhole {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 3mm;

  img {
    max-width: 3.3cm;
    border-radius: 100%;
    max-height: 3.3cm;
    height: 3.3cm;
    width: 3.3cm;
    object-position: center;
    object-fit: cover;
    border: 1mm solid #444;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  font-size: 0.8rem;
  text-align: center;

  small {
    font-size: 0.6rem;
    position: absolute;
    bottom: 1mm;
    right: 2%;
  }
}
</style>
