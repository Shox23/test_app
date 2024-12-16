<template>
  <section class="content">
    <div class="content__header">
      <h3 class="content__title">List of your friends</h3>
      <FilledButton>
        <div class="content__btn">
          <p>Claim</p>
          <div class="content__btn__wrapper">
            <img class="content__btn__icon" src="/images/coin.svg" alt="coin">
            <p>12.5k</p>
          </div>
        </div>
      </FilledButton>
    </div>
    <UserList />
  </section>
</template>

<script lang="ts" setup>
import FilledButton from '../FilledButton/FilledButton.vue';
import UserList from '../UserList/UserList.vue';
</script>

<style lang="scss">
.content {
  display: flex;
  flex-direction: column;
  padding-bottom: 12px;
  gap: 12px;

  @media (max-width: 768px) {
    gap: 4px;
  }

  &__header {
    align-self: center;
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 12px;
    padding-bottom: 8px;

    @media (max-width: 768px) {
      gap: 4px;
    }
  }

  &__title {
    font-weight: 900;
    font-size: 22px;
    font-family: $primary-font;
    color: #fff;
    text-stroke: 0.3px #000;
    -webkit-text-stroke: 0.3px #000;

    @media (max-width: 768px) {
      font-size: 16px;
    }
  }

  &__btn {
    display: flex;
    align-items: center;
    gap: 8px;

    &__icon {
      width: 12px;
      height: 12px;
    }

    &__wrapper {
      display: flex;
      align-items: center;
      gap: 4px;
    }
  }
}
</style>