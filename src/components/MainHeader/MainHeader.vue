<template>
  <header class="main-header">
    <div class="container">
      <h1 class="main-header__title">Invite friends!</h1>
      <h3 class="main-header__subtitle">
        You and your friend will receive bonuses!
      </h3>
    </div>
  </header>
</template>

<script lang="ts" setup></script>

<style lang="scss">
.main-header {
  padding-bottom: 12px;

  &__title {
    text-align: center;
    color: #facb46;
    text-transform: uppercase;
    font-size: 32px;
    -webkit-text-stroke: 0.5px #000;
    text-stroke: 0.5px #000;
    font-family: $accent-font;
    margin-bottom: 4px;
    text-shadow: 0 2px 0 #000;

    @media (max-width: 768px) {
      padding: 24px 0 12px;
      font-size: 24px;
    }
  }

  &__subtitle {
    text-align: center;
    color: #fff;
    font-family: $primary-font;
    font-size: 18px;
    text-shadow: 0 1px 0 #000;

    @media (max-width: 768px) {
      font-size: 14px;
    }
  }
}
</style>
