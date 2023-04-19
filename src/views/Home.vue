<template>
  <div class="flex p-8 flex-col">
    <div >
      <input
        type="text"
        class="rounded border-2 border-gray-200 w-full"
        placeholder="Meals search"
      />
    </div>
    <div class="flex justify-center gap-2 mt-2">
      <router-link :to="{name: 'byLetter', params: {letter}}" v-for="letter of letters" :key="letter">
        {{ letter }}
      </router-link>
    </div>
  </div>
</template>

<script setup>
import { computed, onMounted, ref } from "vue";
import store from "../store";
import axiosClient from '../axiosClient.js'

const letters = "ABCDEFGHIJKLMNOPQRSTUVWSYZ".split("");
const ingredients = ref([]);

onMounted( async () => {
  const response = await axiosClient.get('/list.php?i=list');
  ingredients.value = response.data;
})
</script>

<style></style>
