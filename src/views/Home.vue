<template>
  <div class="flex p-8 flex-col">
   
  </div>
</template>

<script setup>
import { computed, onMounted, ref } from "vue";
import store from "../store";
import axiosClient from '../axiosClient.js'

const ingredients = ref([]);

onMounted( async () => {
  const response = await axiosClient.get('/list.php?i=list');
  ingredients.value = response.data;
})
</script>

<style></style>
