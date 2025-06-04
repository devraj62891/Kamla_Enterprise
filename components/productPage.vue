<template>
  <div class="h-[100vh] items-center">
    <div class="pageDis p-2 text-center text-xl">
      <h1 class="text-3xl font-bold">Products We Manufacture</h1>
    </div>

    <div class="cardSection flex gap-6 justify-center p-3 md:flex-row flex-col items-center pb-3 mb-2">
      <card image="/steep_core.jpg" heading="Steep Core" description="This is a steep core" />
      <card image="/2nd.jpg" heading="unknown" description="some metal thing" />
      <card image="/3rd.jpg" heading="Ei core" description="some mtal thing" />
    </div>

    <div class="shopButon text-center">
      <UButton to="/paiseLaya"
        class="text-2xl bg-blue-300 pl-4 pr-4 pt-2 pb-2 hover:bg-blue-200 hover:cursor-pointer rounded-3xl hover:scale-95 transition-transform mb-2">
        Shop Now
      </UButton>
    </div>

    <div class="mainFoot pt-9 h-[100vh] flex justify-between p-4 md:flex-row flex-col bg-gray-200">
      <div class="address">
        <h1 class="font-bold">OFFICE & FACTORY:</h1>
        <p>237P/1A, SATIN SEN SARANI KAKURGACHI, KOLKATA- 700054</p>
        <h1 class="font-bold mt-10">GODOWN</h1>
        <p>Gr. Floor RAJEN SETH LANE,BELUR BALLY, HOWRAH- 711202</p>
        <div class="tellUs mt-10 ml-10 items-center justify-center align-middle flex">
          <!-- <div>
            <h1 class="font-bold">Feedback</h1>
            
            <UTextarea v-model="value" placeholder="type..." />
            <UButton 
              class="ml-1  bg-blue-200 hover:bg-blue-300 hover:scale-95 transition-transform hover:cursor-pointer"
              label="Send Feedback" color="primary" variant="outline" @click="buttonClicked" />

          </div> -->
           <div>
    <form ref="form" @submit.prevent="sendEmail" class="border rounded p-2 bg-pink-50 flex flex-col items-center">
      <h1 class="font-bold">Feedback</h1>
      <UTextarea
        v-model="message"
        name="message"
        placeholder="your identity will be hidden"
        class="mb-4"
        required
      />
      <input type="submit" value="Send" class="ml-3.5  bg-pink-400 hover:scale-95 hover:bg-pink-500 transition-transform text-white px-4 py-2 rounded cursor-pointer" />
      <div v-if="status" :class="{ 'text-green-600': success, 'text-red-600': !success }" class="mt-2">
        {{ status }}
      </div>
    </form>
  </div>
        </div>
      </div>
      <div class="mapSection items-center">
        <div class="w-full h-[200px] sm:h-[300px] md:h-[400px]">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3683.967385873709!2d88.3809745!3d22.580323099999998!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a027731ffebd9f3%3A0xe15362fabe492802!2sKamala%20Enterprise!5e0!3m2!1sen!2sin!4v1748863954120!5m2!1sen!2sin"
            class="w-full h-full" style="border: 0" allowfullscreen="" loading="lazy">
          </iframe>
        </div>
      </div>
    </div>
    <chat />
  </div>
</template>

<!-- <script setup lang="ts">
// const value = ref('');






// function buttonClicked() {
  

//   if (value.value.trim() == "") {

//     alert("please provide feedback")
//   } else {
//     value.value = '';
//     alert("Thanks for the feedback")
//   }

//   (function(){
//       emailjs.init({
//         publicKey: "YOUR_PUBLIC_KEY",
//       });
//    })();




// }

import emailjs from '@emailjs/browser';


    function sendEmail() {
      emailjs
        .sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this.$refs.form, {
          publicKey: 'YOUR_PUBLIC_KEY',
        })
        .then(
          () => {
            console.log('SUCCESS!');
          },
          (error) => {
            console.log('FAILED...', error.text);
          },
        );
    }
  
</script> -->


<script setup>
import { ref } from 'vue'
import emailjs from '@emailjs/browser'

const form = ref(null)
const message = ref('')
const status = ref('')
const success = ref(false)

const sendEmail = () => {
  if (!message.value.trim()) {
    status.value = 'Please enter a message.'
    success.value = false
    return
  }

  emailjs
    .sendForm('service_94qpepm', 'template_1l75oh9', form.value, {
      publicKey: 'XI0gpTVSC9OA8a3Yc',
    })
    .then(() => {
      status.value = 'Message sent successfully!'
      success.value = true
      message.value = ''
    })
    .catch((error) => {
      status.value = 'Failed to send message.'
      success.value = false
      console.error('EmailJS Error:', error)
    })
}
</script>

