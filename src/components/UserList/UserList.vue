<template>
  <ul class="user-list">
    <li v-for="item in listOfUsers" :key="item.id" class="user-list__item">
      <div class="user-list__profile">
        <img :src="`/images/${item.profileImage ? item.profileImage : defaultImage}`" alt="icon">
        <div class="user-list__name">
          {{ item.name }}
        </div>
      </div>
      <div class="user-list__level">
        {{ `${item.level} lvl` }}
      </div>
    </li>
  </ul>
</template>

<script lang="ts" setup>
import { onBeforeMount } from 'vue';
import users from '../../data/Users';
import User from '../../types/User';

const listOfUsers: User[] = []
const defaultImage: String = "question.png"

onBeforeMount(
  () => {
    listOfUsers.push(...users)
  }
)
</script>

<style lang="scss">
.user-list {
  overflow: hidden;
  position: relative;
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
  border-radius: 12px;
  padding: 16px 8px;
  z-index: 0;
  box-shadow: inset 0 4px 4.5px #000306;

  // &::after {
  //   border-radius: 12px;
  //   position: absolute;
  //   left: 0;
  //   top: 0;
  //   content: '';
  //   width: 100%;
  //   height: 100%;
  //   z-index: 10;
  // }

  @media (max-width: 768px) {
    padding: 6px 3px;
  }

  &__item {
    background: radial-gradient(#3081B4, #19488C, transparent);
    position: relative;
    font-weight: 900;
    font-family: $primary-font;
    color: #fff;
    text-stroke: 0.3px #000;
    -webkit-text-stroke: 0.3px #000;
    padding: 16px 8px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-right: 40px;

    @media (max-width: 768px) {
      padding: 6px 4px;
    }

    &::after {
      position: absolute;
      left: 0;
      bottom: 0;
      content: '';
      height: 1px;
      width: 100%;
      background: radial-gradient(#A7DEFD, rgba(#A7DEFD, 0));
    }
  }

  &__profile {
    display: flex;
    align-items: center;
    gap: 8px;
  }

  &__name {
    font-size: 18px;

    @media (max-width: 768px) {
      font-size: 10px;
    }
  }

  &__level {
    font-size: 20px;

    @media (max-width: 768px) {
      font-size: 16px;
    }
  }
}
</style>