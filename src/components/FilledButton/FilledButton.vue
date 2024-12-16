<template>
  <button class="filled-btn" :class="{ blue: type === 'blue' }">
    <div class="filled-btn__top-outline"></div>
    <slot />
    <div class="filled-btn__bottom-outline"></div>
  </button>
</template>

<script lang="ts" setup>
import FilledButtonProps from "./interfaces";

const { type = "orange" } = defineProps<FilledButtonProps>();
</script>

<style lang="scss">
.filled-btn {
  width: max-content;
  border: none;
  position: relative;
  background: linear-gradient(to right, #f7cb40, #ddad1c);
  display: flex;
  align-items: center;
  height: 26px;
  color: #fff;
  font-size: 16px;
  font-weight: bold;
  height: 30px;
  border-radius: $base-radius;
  padding: 0 24px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.4);
  cursor: pointer;
  transition: transform 0.2s;

  @media (max-width: 768px) {
    padding: 0 20px;
  }

  &:hover {
    transform: scale(1.05);
  }

  &:active {
    transform: scale(0.95);
  }

  &::after {
    content: '';
    right: 5px;
    transform: rotate(22deg);
    top: 0;
    position: absolute;
    width: 8px;
    height: 5px;
    border-radius: 100%;
    background: #ffeeba;
  }

  &__top-outline {
    left: 0;
    top: -2px;
    position: absolute;
    border-radius: $base-radius;
    width: 100%;
    height: 100%;
    background: #ffeeba;
    z-index: -1;
  }

  &__bottom-outline {
    left: 0;
    top: 2px;
    position: absolute;
    border-radius: $base-radius;
    width: 100%;
    height: 100%;
    background: #7a5d00;
    z-index: -1;
  }

  p {
    font-family: $accent-font;
    font-size: 16px;
    text-stroke: 0.3px #1F1F1F;
    -webkit-text-stroke: 0.3px #1F1F1F;

    @media (max-width: 768px) {
      font-size: 12px;
    }
  }
}

.filled-btn.blue {
  background: linear-gradient(to right, #44a2e5, #2e7ec2);

  .filled-btn__top-outline {
    background: #bee3ff;
  }

  .filled-btn__bottom-outline {
    background: #115388;
  }

  &::after {
    background: #bee3ff;
  }
}
</style>
