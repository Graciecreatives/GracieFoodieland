<template>
  <section class="px-5 py-10 md:px-10 lg:px-20">
    <!-- Header section -->
    <div class="flex flex-col md:flex-row md:justify-between md:items-center md:gap-10 mb-10 text-center md:text-left">
      <h2 class="text-2xl sm:text-3xl md:text-4xl font-semibold leading-snug md:w-1/2">
        Try this delicious recipe to make your day
      </h2>
      <p class="text-gray-600 mt-3 md:mt-0 md:w-1/2">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </div>

    <!-- Recipe grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
      <div
        v-for="recipe in recipes"
        :key="recipe.id"
        class="bg-white rounded-xl shadow-sm hover:shadow-md transition-all duration-300 p-3"
      >
        <div class="relative mb-3">
          <img
            :src="recipe.image"
            :alt="recipe.content"
            class="rounded-lg w-full h-60 object-cover"
          />
          <button
            @click="toggleLike(recipe)"
            class="absolute top-4 right-4 bg-white/80 p-2 rounded-full hover:scale-110 transition-transform"
          >
            <span v-if="recipe.liked">
              <img src="../assets/Images/RecipeImages/heartlove.png" alt="liked" class="w-5 h-5" />
            </span>
            <span v-else>
              <img src="../assets/Images/RecipeImages/heart.png" alt="not liked" class="w-5 h-5" />
            </span>
          </button>
        </div>

        <h3 class="font-medium text-lg leading-snug mb-2">
          {{ recipe.content }}
        </h3>

        <div class="flex justify-between items-center text-gray-500 text-sm mt-3">
          <span class="inline-flex items-center gap-2">
            <img src="../assets/Images/Timer.png" alt="" class="w-4 h-4" />
            {{ recipe.time }}
          </span>
          <span class="inline-flex items-center gap-2">
            <img src="../assets/Images/ForkKnife.png" alt="" class="w-4 h-4" />
            {{ recipe.category }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

import TropicalFruitSalad from "../assets/Images/deliciousRecipeImage/tropical fruit.png";
import wagyu from "../assets/Images/deliciousRecipeImage/wagyu.png";
import JapaneseRice from "../assets/Images/deliciousRecipeImage/japanese.png";
import walnut from "../assets/Images/deliciousRecipeImage/walnut.png";
import rainbowChicken from "../assets/Images/deliciousRecipeImage/rainbowChicken.png";
import spiySandwich from "../assets/Images/deliciousRecipeImage/spicySandwish.png";
import fineCracker from "../assets/Images/deliciousRecipeImage/fineCracker.png";
import chickenRamen from "../assets/Images/deliciousRecipeImage/chickenRamen.png";

const toggleLike = (recipe) => {
  recipe.liked = !recipe.liked;
};

const recipes = ref([
  {
    id: 1,
    image: TropicalFruitSalad,
    content: "Mixed Tropical Fruit Salad with Superfood Boosts",
    time: "30 Minutes",
    category: "Healthy",
    liked: true,
  },
  {
    id: 2,
    image: wagyu,
    content: "Big and Juicy Wagyu Beef Cheeseburger",
    time: "30 Minutes",
    category: "Western",
    liked: false,
  },
  {
    id: 3,
    image: JapaneseRice,
    content: "Healthy Japanese Fried Rice with Asparagus",
    time: "30 Minutes",
    category: "Healthy",
    liked: false,
  },
  {
    id: 4,
    image: walnut,
    content: "Cauliflower Walnut Vegetarian Taco Meat",
    time: "30 Minutes",
    category: "Eastern",
    liked: false,
  },
  {
    id: 5,
    image: rainbowChicken,
    content: "Rainbow Chicken Salad with Almond Honey Mustard Dressing",
    time: "30 Minutes",
    category: "Healthy",
    liked: false,
  },
  {
    id: 6,
    image: spiySandwich,
    content: "Barbeque Spicy Sandwiches with Chips",
    time: "30 Minutes",
    category: "Snack",
    liked: false,
  },
  {
    id: 7,
    image: fineCracker,
    content: "Firecracker Vegan Lettuce Wraps - Spicy!",
    time: "30 Minutes",
    category: "SeaFood",
    liked: false,
  },
  {
    id: 8,
    image: chickenRamen,
    content: "Chicken Ramen Soup with Mushroom",
    time: "30 Minutes",
    category: "Japanese",
    liked: false,
  },
]);
</script>

<style scoped>
/* Optional: smooth scaling for cards */
@media (hover: hover) {
  .hover\:shadow-md:hover {
    transform: translateY(-2px);
  }
}
</style>
