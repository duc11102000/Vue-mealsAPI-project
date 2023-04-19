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
      <router-link to="/" v-for="letter of letters">
        {{ letter }}
      </router-link>
    </div>
  </div>
</template>

<script setup>
import { computed } from "vue";
import store from "../store";

const meals = computed(() => store.state.meals);
const letters = "ABCDEFGHIJKLMNOPQRSTUVWSYZ".split("");
</script>

<style></style>
