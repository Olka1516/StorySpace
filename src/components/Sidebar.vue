<script lang="ts" setup>
import { inject, type Ref } from 'vue'

const { isMenuOpen, updateMenu } = inject<{
  isMenuOpen: Ref<boolean>
  updateMenu: () => void
}>('menu')!
</script>

<template>
  <div class="sidebar" :class="{ close: !isMenuOpen }">
    <div class="sidebar-top">
      <button @click="updateMenu">
        <img src="@/assets/pictures/icons/exit.png" alt="" />
      </button>
    </div>
    <a href="#home">Home</a>
    <a href="#news">News</a>
    <a href="#contact">Contact</a>
    <a href="#about">About</a>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/index';
@include index.sidebar;
</style>
