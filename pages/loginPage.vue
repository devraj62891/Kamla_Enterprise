<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-100">
    <div class="bg-white p-8 rounded-lg shadow-md w-full max-w-sm">
      <h2 class="text-2xl font-bold mb-6 text-center text-gray-800">Login</h2>

      <form class="space-y-4" @submit.prevent="handleLogin">
        <div>
          <label class="block text-sm font-medium text-gray-600 mb-1">Username</label>
          <input v-model="username"
            type="text"
            placeholder="Enter your username"
            class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <div>
          <label class="block text-sm font-medium text-gray-600 mb-1">Password</label>
          <input v-model="password"
            type="password"
            placeholder="Enter your password"
            class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <button
          type="submit"
          class="w-full bg-blue-600 hover:cursor-pointer text-white py-2 rounded-md hover:bg-blue-700 transition"
        >
          Login
        </button>
      </form>
    </div>
  </div>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'custom'
})

const username=ref('');
const password=ref('');
const router=useRouter();



//since i have no bacend now 
const noBack=ref(true);

// async function handleLogin(){


//   try {
//     if(noBack){
//       router.push({path:"/adminPage"})
//     }
//     else{
//       const res= await $fetch('api/login',{
//       method:'POST',
//       body:{
//         username:username.value,
//         password:password.value
//       }
//     })
    
//     // router.push({ path: "/adminPage" })
//     await navigateTo("/adminPage")
    
//     }
    
    
//   } catch (err) {
//     console.log("Login error:",err);
//     alert("login failed")
    
    
//   }
// }

function handleLogin(){
  if(username.value=="abhi1234" && password.value=="9999"){
    navigateTo("/adminPage")
  }else{
    navigateTo("/");
    alert("login failed")
  }
}





</script>