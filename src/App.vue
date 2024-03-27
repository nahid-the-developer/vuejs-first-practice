<script setup>
import { RouterView } from 'vue-router'
import Navbar from '@/components/Navbar.vue'
</script>

<template>
  <Navbar />
  <div class="max-w-[1216px] w-full m-auto px-4 md:px-0 mt-[96px]">
    <RouterView />
  </div>
</template>

<style></style>
