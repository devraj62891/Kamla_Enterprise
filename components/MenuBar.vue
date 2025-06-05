<template>
  <div class="bg-gray-200 p-4 flex flex-col md:flex-row md:items-center md:justify-between space-y-4 md:space-y-0">

    <div class="flex justify-center md:justify-start">
      <img class="h-24 w-24 rounded-full" src="/public/brand.png" alt="Brand Logo" />
    </div>


    <div class="text-center md:text-center md:flex-1">
      <p class="text-lg md:text-2xl font-bold">
        Deals in: Transformer Core, E/L, Steel Core, CT Core
      </p>
    </div>


    <div class="flex flex-wrap justify-center md:justify-end gap-2 md:gap-4">
      <ul class="hover:underline hover:text-gray-700 p-2 rounded-md">
        <NuxtLink to="/aboutPage">About</NuxtLink>
      </ul>
      <ul class="hover:underline hover:text-gray-700 p-2 rounded-md">
        <NuxtLink to="/productPage">All Products</NuxtLink>
      </ul>
      <ul class="hover:underline hover:text-gray-700 p-2 rounded-md">
        <NuxtLink to="/contactPage">Contact</NuxtLink>
      </ul>
      <ul  class="hover:underline hover:text-gray-700 p-2 rounded-md text-red-500">
        <NuxtLink  to="/loginPage">Admin</NuxtLink>
      </ul>
      
    </div>

  </div>
</template>


<script setup>
import { UButton } from '#components';

</script>
