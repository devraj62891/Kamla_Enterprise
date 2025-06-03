<template>
    <div>
        <div v-if="showChat" @click="showChat = false" class="fixed left-0 right-0 bottom-0 top-0 bg-transparent"></div>
        <!-- Chat Box -->
        <div v-if="showChat" class="  fixed bottom-24 right-6 bg-green-200 w-74 h-100 p-4 shadow-lg rounded ">
            Coming soon...

        </div>
        
            

        <!-- Chat Button -->
        <UButton @click="chatButtonClick"
            class="bg-blue-300 fixed bottom-12 right-6 rounded-xl hover:scale-95 hover:bg-blue-500 transition-transform hover:cursor-pointer">
            Chat
        </UButton>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const showChat = ref < boolean > (false)

function chatButtonClick() {
    showChat.value = !showChat.value
}
</script>
