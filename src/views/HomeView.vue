<template>
  <main>
    <!-- <HomeSection/> -->
    <!-- <TheWelcome /> -->

    <!-- Category Section -->
    <section class="categorySection px-5 py-5 md:px-10 md:py-10">
      <div class="flex justify-between items-center gap-10 mb-5 md:mb-10">
    <h2 class="text-3xl md:text-5xl font-[600]">Categories</h2>
    <router-link to="" class="bg-[#e7f9fd] rounded-lg p-2 text-sm">View All Categories</router-link>
    </div>

    <div class="grid grid-cols-3 sm:grid-cols-3 lg:grid-cols-6 gap-6 md:gap-10">
      <div v-for="category in categories" :key="category.id" :style="{backgroundImage: `url(${category.background})`}" class="p-3 px-1  text-center bg-cover bg-center rounded-lg">
        <img :src="category.image" alt="" class="md:w-25 w-10 mb-5 mx-auto">
        <p class="text-sm md:text-base">{{ category.text }}</p>

      </div>
    </div>
    </section>
    <simpleRecipe/>

    <!--Kitchen CHef Section-->
    <section class="px-5 py-5 md:px-10 md:py-10 flex flex-col md:flex-row items-center gap-10">
      <div class="w-full md:w-1/2">
        <h2 class="md:text-5xl/17 text-3xl/10 font-[600] md:mb-5 mb-3">Everyone can be a chef in their own kitchen</h2>
        <p class="mb-5">Lorem ipsum dolor sit amet, consectetuipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqut enim ad minim </p>
        <router-link to="" class="bg-black text-white text-center px-4 py-2 rounded-lg">Learn More</router-link>
      </div>

      <div class="w-full md:w-1/2">
        <img src="../assets/Images/kitchenChef.png" alt="">
      </div>
    </section>
    <foodieInstagram/>
    <deliciousRecipe/>
  </main>
</template>

<script setup>

// import HomeSection from '@/components/HomeSection.vue';
import simpleRecipe from '@/components/simpleRecipe.vue'
import foodieInstagram from '@/components/foodieInstagram.vue'
import deliciousRecipe from '@/components/deliciousRecipe.vue'
import BreakfastBg from '../assets/Images/breakfastBackground.png'
import Breakfast from '../assets/Images/Breakfast.png'
import VeganBg from '../assets/Images/veganBackground.png'
import Vegan from '../assets/Images/Vegan.png'
import meatBg from '../assets/Images/meatBackground.png'
import meat from '../assets/Images/meat.png'
import desertBg from '../assets/Images/desertBG.png'
import desert from '../assets/Images/Desert.png'
import LunchBg from '../assets/Images/LunchBg.png'
import Lunch from '../assets/Images/Lunch.png'
import chocolateBg from '../assets/Images/chocolateBg.png'
import chocolate from '../assets/Images/chocolate.png'
const categories = [
  {
    id: 1,
    background: BreakfastBg,
    image: Breakfast,
    text: 'Breakfast'
  },

  {
    id: 2,
    background: VeganBg,
    image: Vegan,
    text: 'Vegan'
  },

  {
     id: 3,
    background: meatBg,
    image: meat,
    text: 'Meat'
  },

   {
     id: 4,
    background: desertBg,
    image: desert,
    text: 'Desert'
  },

    {
     id: 5,
    background: LunchBg,
    image: Lunch,
    text: 'Lunch'
  },

  {
     id: 6,
    background: chocolateBg,
    image: chocolate,
    text: 'Chocolate'
  }
]
</script>

<style scoped>
</style>
