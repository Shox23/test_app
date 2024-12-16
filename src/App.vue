<script setup lang="ts">
import ContentSection from "./components/ContentSection/ContentSection.vue";
import HeroSection from "./components/HeroSection/HeroSection.vue";
import MainHeader from "./components/MainHeader/MainHeader.vue";
</script>

<template>
  <div class="app">
    <MainHeader />
    <div class="container app__content">
      <HeroSection />
      <ContentSection />
    </div>
  </div>
</template>

<style lang="scss">
.app {
  background: radial-gradient(#3081B4, #19488C);

  &__content {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
}
</style>