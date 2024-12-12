<script setup lang="ts">
import HeroSection from "./components/HeroSection/HeroSection.vue";
import MainHeader from "./components/MainHeader/MainHeader.vue";
</script>

<template>
  <div>
    <MainHeader />
    <div class="container">
      <HeroSection />
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
