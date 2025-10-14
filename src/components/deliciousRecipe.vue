<template>
  <section class="px-5 py-5 md:px-10 md:py-10">
    <h2>Try this delicious recipe to make your day</h2>
    <p>Lorem ipsum dolor sit amet, consectetuipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqut enim ad minim </p>

<div class="grid grid-cols-1 md:grid-cols-4 gap-10">
    <div v-for="recipe in recipes" :key="recipe.id">
      <div class="relative mb-3">
      <img :src="recipe.image" :alt="recipe.content" class="rounded-lg" />
      <button @click="toggleLike(recipe)" class="absolute top-5 right-3">
        <span v-if="recipe.liked"><img src="../assets/Images/RecipeImages/heartlove.png" alt=""></span>
        <span v-else><img src="../assets/Images/RecipeImages/heart.png" alt=""></span>
      </button>
      </div>
      <h3>{{ recipe.content }}</h3>
      <div class="flex justify-between mt-3">
            <span class="inline-flex items-center gap-2"><img src="../assets/Images/Timer.png" alt="" class="w-5">{{ recipe.time }}</span>

            <span class="inline-flex items-center gap-2"><img src="../assets/Images/ForkKnife.png" alt="" class="w-5">{{ recipe.category }}</span>
          </div>
    </div>
    </div>
  </section>
</template>

<script setup>
import { ref  } from "vue";

import TropicalFruitSalad from '../assets/Images/deliciousRecipeImage/tropical fruit.png'
import wagyu from '../assets/Images/deliciousRecipeImage/waguy.png'
import JapaneseRice from '../assets/Images/deliciousRecipeImage/japanese.png'

const toggleLike = (recipe) => {
  recipe.liked = !recipe.liked;
}
const recipes = ref([
{
  id: 1,
  image: TropicalFruitSalad,
  content: "Mixed Tropical Fruit Salad with Superfood Boosts",
  time: "30 Minutes",
  category: "Healthy",
  liked: true
},

{
  id: 2,
  image: wagyu,
  content: "Big and Juicy Wagyu Beef Cheeseburger",
  time: "30 Minutes",
  category: "Western",
   liked: false
},

{
  id: 3,
  image: JapaneseRice,
  content: "Healthy Japanese Fried Rice with Asparagus",
  time: "30 Minutes",
  category: "Healthy",
   liked: false
},

{
  id: 4,
  image: TropicalFruitSalad,
  content: "Cauliflower Walnut Vegetarian Taco Meat",
  time: "30 Minutes",
  category: "Eastern",
   liked: false
},

{
  id: 5,
  image: TropicalFruitSalad,
  content: "Rainbow Chicken Salad with Almond Honey Mustard Dressing",
  time: "30 Minutes",
  category: "Healthy",
   liked: false
},

{
  id: 6,
  image: TropicalFruitSalad,
  content: "Mixed Tropical Fruit Salad with Superfood Boosts",
  time: "30 Minutes",
  category: "Healthy",
   liked: false
},

{
  id: 7,
  image: TropicalFruitSalad,
  content: "Mixed Tropical Fruit Salad with Superfood Boosts",
  time: "30 Minutes",
  category: "Healthy",
   liked: false
},

{
  id: 8,
  image: TropicalFruitSalad,
  content: "Mixed Tropical Fruit Salad with Superfood Boosts",
  time: "30 Minutes",
  category: "Healthy",
   liked: false
}
])
</script>

<style scoped>
</style>
