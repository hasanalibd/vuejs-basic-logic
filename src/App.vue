<script setup>
const location = 'Dhaka'
const weather = 't'
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Logic in Vue.js</h1>
    <div class="w-1/2 bg-gray-200 p-10 flex items-center flex-col space-y-10">
      <h1 class="text-3xl">{{ location }}</h1>

      <template v-if="weather=='s'">
          <h2 class="text-2xl" >Weather: Sunny</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7911203/weather-icon-md.png" alt="">
      </template>
      
      <template v-if="weather=='pc'">
          <h2 class="text-2xl">Weather: Partly Cloudy</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912718/weather-icon-md.png" alt="">
      </template>

      <template v-if="weather=='r'">
          <h2 class="text-2xl" >Weather: Rainy</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7913380/weather-icon-md.png" alt="">
      </template>

      <template v-if="weather=='t'">
          <h2 class="text-2xl" >Weather: Thunderstorm</h2>
          <img src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912589/weather-icon-md.png" alt="">
      </template>
      <!-- 
        যদি একই কন্ডিশনের ভিতর একাধিক ট্যাগ পরে তাহলে সেগুলোকে একটা নোডের ভিতর রাখতে হয়। গ্রুপের করার ক্ষেত্রে সবশ্যই invisiable tag যেমন <template> </template> এর ভিতর উপাদান গুলোকে রাখতে হবে। তবে template নোডের ক্ষেত্রে শুধু v-if সাপোর্ট করে । <template> </template> এর সাথে v-show ব্যবহার করা যাই না। 
       -->
    </div>
  </section>
</template>

<style scoped></style>