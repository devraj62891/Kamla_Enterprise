<template>
    <div>
        <div v-if="showChat" @click="showChat = false" class="fixed left-0 right-0 bottom-0 top-0 bg-transparent"></div>
        <!-- Chat Box -->
        <div  v-if="showChat" class="fixed bottom-30 right-6 bg-green-200 w-74 h-100 p-4 shadow-lg rounded">
            <div class="iconPlace flex items-center gap-2 h-10 mb-1">
                <div class="bg-white rounded-2xl ml-1 z-50 shadow-orange-700">
                    <UIcon class="pt-3 mt-1 text-2xl " name="material-symbols:robot-2-sharp"></UIcon>
                </div>
                <span class="font-bold">KamlaBot</span>
            </div>

            <div class="chatContainer bg-white h-[40vh] md:h-[50vh] p-1 rounded overflow-y-auto ">
                <div class="bg-blue-200 p-2 mt-2 rounded text-sm text-green-800">
                    👉 Choose one of the options below:
                </div>

                <div @click="alertConstruction" class="list">
                    <ul>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">First</li>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">help</li>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">help</li>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">First</li>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">First</li>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">First</li>
                        <li class="bg-blue-200 m-1 p-2 hover:scale-105 hover:bg-green-300 hover:cursor-pointer rounded-2xl">First</li>


                    </ul>
                </div>
            </div>
        </div>

        <!-- Chat Button -->
        <UButton @click="chatButtonClick"
            class="bg-green-300 fixed w-15 h-12 shadow-2xl bottom-12 right-6 rounded-xl hover:scale-95 hover:bg-green-500 transition-transform hover:cursor-pointer">
            <Icon class="text-3xl items-center" name="material-symbols:android" />
        </UButton>
    </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const showChat = ref<boolean>(false);

function chatButtonClick() {
    showChat.value = !showChat.value;
}

function alertConstruction(){
    alert("under construction");
}



</script>
