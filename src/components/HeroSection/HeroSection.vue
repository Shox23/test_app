<script setup lang="ts">
import FilledButton from "../FilledButton/FilledButton.vue";
</script>

<template>
  <section class="hero-section">
    <div class="container">
      <div class="hero-section__grid">
        <div class="hero-section__cell">
          <img
            class="hero-section__cell__img"
            src="/images/first-cell.jpg"
            alt="background"
          />
          <div class="hero-section__cell__btn">
            <FilledButton>
              <p>More Bonuses</p>
            </FilledButton>
          </div>
        </div>
        <div class="hero-section__cell">
          <img
            class="hero-section__cell__img"
            src="/images/second-cell.jpg"
            alt="background"
          />
          <div class="hero-section__cell__btn">
            <FilledButton type="blue">
              <p>Invite</p>
            </FilledButton>
            <FilledButton type="blue">
              <div><img src="/images/currency.svg" alt="icon  " /></div>
            </FilledButton>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.hero-section {
  &__grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
  }

  &__cell {
    position: relative;
    display: flex;
    align-items: flex-end;
    justify-content: center;
    overflow: hidden;
    border-radius: $base-radius;
    border: 2px solid #7dd0ff;

    &__img {
      width: 100%;
      height: 100%;
    }

    &__btn {
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translateX(-50%);

      &:last-child {
        display: flex;
        gap: 16px;
      }
    }
  }
}
</style>
