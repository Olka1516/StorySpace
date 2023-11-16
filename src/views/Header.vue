<script setup lang="ts">
import { inject } from 'vue'
import Search from '@/components/Search.vue'

const { updateMenu } = inject<{
  updateMenu: () => void
}>('menu')!

const test = () => {
  console.log('hello')
}
</script>

<template>
  <div class="container">
    <header>
      <div class="content content-items">
        <button @click="updateMenu">
          <img src="@/assets/pictures/icons/menu.png" alt="" />
        </button>
        <img class="logo" src="@/assets/pictures/logo_with_text.png" alt="Logo" />
      </div>
        <Search />
      <button class="account-button" @click="test">
        <img class="account-image" src="@/assets/pictures/book.jpg" alt="" />
      </button>
    </header>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/index';
@include index.header;
</style>
