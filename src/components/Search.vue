<script setup lang="ts">
const search = () => {
  console.log('search')
}
</script>

<template>
    <button class="search-button" @click="search"></button>
        <input type="text" placeholder="Search" style="vertical-align: middle" />
</template>