<template>
  <section class="simpleRecipeSection px-5 py-5 md:px-10 md:py-10">
    <h2 class="md:text-4xl font-[600] text-center mb-3">Simple and tasty recipes</h2>
    <p
      class="md:w-170 text-center mx-auto md:mb-10"
    >Lorem ipsum dolor sit amet, consectetuipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqut enim ad minim</p>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
      <template v-for="(recipe, index) in Recipes" :key="recipe.id">
        <div class="bg-[#E7F9FD] p-3 rounded-lg">
          <div class="relative">
            <img :src="recipe.image" alt="" class="rounded-xl" />
            <button @click="toggleLike(recipe)" class="absolute top-5 right-5">
              <span v-if="recipe.liked">
                <img src="../assets/Images/RecipeImages/heartlove.png" alt />
              </span>
              <span v-else>
                <img src="../assets/Images/RecipeImages/heart.png" alt />
              </span>
            </button>
          </div>
          <h3 class="md:text-2xl text-xl font-[500] mt-3">{{ recipe.content }}</h3>
          <div class="flex justify-between mt-5">
            <span class="inline-flex items-center gap-2"><img src="../assets/Images/Timer.png" alt="" class="w-5">{{ recipe.time }}</span>

            <span class="inline-flex items-center gap-2"><img src="../assets/Images/ForkKnife.png" alt="" class="w-5">{{ recipe.category }}</span>
          </div>
        </div>

        <div v-if="index === 4">
          <img src="../assets//Images/RecipeImages/Ads.png" alt/>
        </div>
      </template>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import wagyuBeef from "../assets/Images/RecipeImages/wagyubeef.png";
import roastedSalmon from "../assets/Images/RecipeImages/roastedSalmon.png";
import strawberryOat from "../assets/Images/RecipeImages/strawberryOat.png";
import MayonnaiseSalad from "../assets/Images/RecipeImages/Mayonnaise Salad.png";
import chickenMeatball from "../assets/Images/RecipeImages/chickenMeatball.png";
import fruityPancake from "../assets/Images/RecipeImages/fruityPancake.png";
import potChicken from '../assets/Images/RecipeImages/potChicken.png'
import Noodles from '../assets/Images/RecipeImages/noodles.png'
const toggleLike = recipe => {
  recipe.liked = !recipe.liked;
};
const Recipes = ref([
  {
    id: 1,
    image: wagyuBeef,
    content: "Big and Juicy Wagyu Beef Cheeseburger",
    time: "30 Minutes",
    category: "Snack",
    liked: true
  },

  {
    id: 2,
    image: roastedSalmon,
    content: "Fresh Lime Roasted Salmon with Ginger Sauce",
    time: "30 Minutes",
    category: "Fish",
    liked: false
  },

  {
    id: 3,
    image: strawberryOat,
    content: "Strawberry Oatmeal Pancake with Honey Syrup",
    time: "30 Minutes",
    category: "Breakfast",
    liked: false
  },

  {
    id: 4,
    image: MayonnaiseSalad,
    content: "Fresh and Healthy Mixed Mayonnaise Salad",
    time: "30 Minutes",
    category: "Healthy",
    liked: false
  },

  {
    id: 5,
    image: chickenMeatball,
    content: "Chicken Meatballs with Cream Cheese",
    time: "30 Minutes",
    category: "Meat",
    liked: false
  },

  {
    id: 6,
    image: fruityPancake,
    content: "Fruity Pancake with Orange & Blueberry",
    time: "30 Minutes",
    category: "Sweet",
    liked: false
  },

   {
    id: 7,
    image: potChicken,
    content: "The Best Easy One Pot Chicken and Rice",
    time: "30 Minutes",
    category: "Snack",
    liked: false
  },


   {
    id: 8,
    image: Noodles,
    content: "The Creamiest Creamy Chicken and Bacon Pasta",
    time: "30 Minutes",
    category: "Noodles",
    liked: false
  }
]);
</script>

<style scoped>
</style>
