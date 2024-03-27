<script setup>
import { ref } from 'vue'

const myInput = ref(null)
const data = ref([])

const submitHandler = (e) => {
  e.preventDefault()
  data.value = [...data.value, myInput.value]
}

</script>

<template>
  <div class="h-[calc(100vh-96px)] w-full flex justify-center items-center flex-col">

    <div class="w-1/3">
      <p class="mb-4 break-all"><span class="font-bold">Input preview:</span> {{ myInput }}</p>
      <form @submit="submitHandler" class="flex items-center gap-x-3">
        <input
          class="shadow appearance-none border rounded w-full p-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="username" type="text" placeholder="Input" v-model="myInput" />

        <button type="submit"
                class="bg-indigo-400 h-11 px-8 rounded-lg font-semibold text-white hover:bg-indigo-300 transition ease-in-out">
          Submit
        </button>
      </form>
    </div>


    <div class="w-1/3 mt-5">
      <ul>
        <template v-for="(item, index) in data" :key="index">
          <li class="w-full bg-gray-200 mb-2 last:mb-0 p-5 rounded-md">{{ item }}</li>
        </template>
      </ul>
    </div>
  </div>


</template>
