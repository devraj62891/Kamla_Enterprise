<template>
    <div class="max-w-sm rounded-2xl overflow-hidden shadow-lg bg-gray-300 p-2 hover:scale-105 transition-transform ">
        <img class="w-40 h-30 object-cover rounded-2xl" :src="image" alt="Card Image" />
        <div class="p-4">
            <h3 class="text-xl font-semibold mb-2">{{ heading }}</h3>
            <p class="text-gray-600 text-sm">
               {{ description }}
            </p>
        </div>
    </div>

</template>

<script setup>
defineProps({
    image:{
        type:String,
        required:true
    },
    heading:{
        type:String,
        required:true
    },
    description:{
        type:String,
        required:true
    }
})

</script>