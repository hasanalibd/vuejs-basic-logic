<script setup>
import {ref} from 'vue'
const location = 'Dhaka'
const weather = ref('s')


</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Logic in Vue.js</h1>
    <div class="w-1/2 bg-gray-200 p-10 flex items-center flex-col space-y-10 mb-5">
      <h1 class="text-3xl">{{ location }}</h1>

      <div v-show="weather=='s'">
          <h2 class="text-2xl" >Weather: Sunny</h2>
          <img id="sunny" src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7911203/weather-icon-md.png" alt="">
      </div>
      
      <div v-show="weather=='pc'">
          <h2 class="text-2xl">Weather: Partly Cloudy</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912718/weather-icon-md.png" alt="">
      </div>

      <div v-show="weather=='r'">
          <h2 class="text-2xl" >Weather: Rainy</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7913380/weather-icon-md.png" alt="">
      </div>

      <div v-show="weather=='t'">
          <h2 class="text-2xl" >Weather: Thunderstorm</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912589/weather-icon-md.png" alt="">
      </div>
      <!-- 
        যদি একই কন্ডিশনের ভিতর একাধিক ট্যাগ পরে তাহলে সেগুলোকে একটা নোডের ভিতর রাখতে হয়। গ্রুপের করার ক্ষেত্রে সবশ্যই invisiable tag যেমন <div> </div> এর ভিতর উপাদান গুলোকে রাখতে হবে। তবে div নোডের ক্ষেত্রে শুধু v-show সাপোর্ট করে । <div> </div> এর সাথে v-show ব্যবহার করা যাই না। 
       -->
    </div>
    <input type="text" name="" id="" v-model="weather" class="text-center border-2 py-2 rounded-lg" placeholder="weather status">
  </section>
</template>

<style scoped></style>