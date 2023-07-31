<template>
  <div class="bg-gray-100 h-full">
    <navbar></navbar>
    <main>
      <h1 class="text-2xl font-bold flex justify-center align-center">Please search meals by name or by letter</h1>
      <router-view />
    </main>
  </div>
</template>

<script setup>
import Navbar from './Navbar.vue'
</script>
