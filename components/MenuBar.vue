<template>
    <div class="bg-gray-200 p-4 md:flex items-center-safe text-wrap">
        <div class="brand ">
            <img class="h-[100px] w-[100px] rounded-full ml-10 " src="/public/brand.png" alt="">
        </div>
        <div class="relative left-[100px] wrap-normal font-bold">
            <p class=" text-2xl">Deals in: Transformer Core,E/L, Steel Core, CT Core</p>
        </div>
        <div class=" md:flex gap-4 relative left-[300px] ">

            <ul class="hover:underline hover:text-gray-700  p-2 rounded-md">
                <NuxtLink to="/aboutPage">About</NuxtLink>
            </ul>
            <ul class="hover:underline hover:text-gray-700  p-2 rounded-md">
                <NuxtLink to="/productPage">All Products</NuxtLink>

            </ul>
            <ul class="hover:underline hover:text-gray-700  p-2 rounded-md">
                <NuxtLink to="/contactPage">Contact</NuxtLink>

            </ul>
            <ul class="hover:underline hover:text-gray-700  p-2 rounded-md ">
                <NuxtLink to="/morePage">More></NuxtLink>
            </ul>
        </div>

        
    </div>
</template>




<script setup lang="ts">
import type { DropdownMenuItem } from '@nuxt/ui'

const items = ref<DropdownMenuItem[]>([
    {
        label: 'Profile',
        icon: 'i-lucide-user'
    },
    {
        label: 'Billing',
        icon: 'i-lucide-credit-card'
    },
    {
        label: 'Settings',
        icon: 'i-lucide-cog'
    }
])
</script>
