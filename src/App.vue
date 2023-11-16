<script setup lang="ts">
import { RouterView } from 'vue-router'
import Header from './views/Header.vue'
import Sidebar from '@/components/Sidebar.vue'
import { provide, ref, type Ref } from 'vue'

const isMenuOpen = ref(false)

const updateMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
const test: {
  isMenuOpen: Ref<boolean>
  updateMenu: () => void
} = { isMenuOpen, updateMenu }

provide('menu', test)
</script>

<template>
  <Header />
  <Sidebar />
  <!-- <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink> -->
  <RouterView />
</template>
