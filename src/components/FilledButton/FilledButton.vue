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
  border: none;
  position: relative;
  background: linear-gradient(to right, #f7cb40, #ddad1c);
  padding: 0 16px;
  display: flex;
  align-items: center;
  height: 26px;
  color: #fff;
  font-size: 16px;
  font-weight: bold;
  border-radius: $base-radius;
  padding: 10px 20px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.4);
  cursor: pointer;
  transition: transform 0.2s, box-shadow 0.2s;

  &:hover {
    transform: scale(1.05);
  }

  &:active {
    transform: scale(0.95);
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
}

.filled-btn.blue {
  background: linear-gradient(to right, #44a2e5, #2e7ec2);

  .filled-btn__top-outline {
    background: #bee3ff;
  }

  .filled-btn__bottom-outline {
    background: #115388;
  }
}
</style>
