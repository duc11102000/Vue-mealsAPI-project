<template>
  <header class="bg-white shadow h-16 flex justify-between items-stretch">
    <router-link
      :to="{ name: 'home' }"
      class="inline-flex items-center h-full px-5"
    >
      Home
    </router-link>
    <div class="flex items-center gap-1">
      <router-link
        :to="{ name: 'byName' }"
        class="inline-flex items-center px-2 h-full hover:bg-orange-500"
      >
        Search meals
      </router-link>
      <router-link
        :to="{ name: 'byLetter' }"
        class="inline-flex items-center px-2 h-full hover:bg-orange-500"
      >
        Meals by letter
      </router-link>
      <!-- <router-link
        :to="{ name: 'ingredients' }"
        class="inline-flex items-center px-2 h-full hover:bg-purple-200"
      >
        Meals by ingredients
      </router-link> -->
    </div>
  </header>
</template>
