<script setup>
const links = [
  {
    label: 'Home',
    path: '/'
  },
  {
    label: 'About',
    path: '/about'
  }
]
</script>

<template>
  <div class="py-8 bg-indigo-400 fixed top-0 w-full">
    <nav class="flex justify-between items-center max-w-[1216px] w-full m-auto px-4 md:px-0">
      <div>
        <router-link to="/" class="text-2xl font-bold">
          logo
        </router-link>
      </div>
      <ul class="flex gap-5 font-bold">
        <li v-for="(link, index) in links" :key="index">
          <router-link :to="link.path" :class="{ 'border-b-2 border-black': $route.path === link.path }">{{ link.label }}</router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

