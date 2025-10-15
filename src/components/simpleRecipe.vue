<template>
  <section class="simpleRecipeSection px-4 sm:px-6 md:px-10 py-8 md:py-12 lg:py-16">
    <h2 class="text-2xl sm:text-3xl md:text-4xl font-[600] text-center mb-3 sm:mb-5">
      Simple and tasty recipes
    </h2>
    <p
      class="max-w-xl sm:max-w-2xl text-center mx-auto mb-6 sm:mb-8 md:mb-10 text-sm sm:text-base leading-relaxed"
    >
      Lorem ipsum dolor sit amet, consectetuipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqut enim ad minim
    </p>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 md:gap-10">
      <template v-for="(recipe, index) in Recipes" :key="recipe.id">
        <!-- Recipe Card -->
        <div class="bg-[#E7F9FD] p-3 sm:p-4 rounded-lg hover:shadow-md transition-shadow duration-300">
          <div class="relative">
            <img
              :src="recipe.image"
              alt=""
              class="rounded-xl w-full h-auto object-cover"
            />
            <button
              @click="toggleLike(recipe)"
              class="absolute top-3 right-3 sm:top-5 sm:right-5"
            >
              <span v-if="recipe.liked">
                <img src="../assets/Images/RecipeImages/heartlove.png" alt />
              </span>
              <span v-else>
                <img src="../assets/Images/RecipeImages/heart.png" alt />
              </span>
            </button>
          </div>

          <h3 class="text-lg sm:text-xl md:text-2xl font-[500] mt-3 sm:mt-4">
            {{ recipe.content }}
          </h3>

          <div class="flex justify-between items-center mt-4 sm:mt-5 text-sm sm:text-base">
            <span class="inline-flex items-center gap-2">
              <img src="../assets/Images/Timer.png" alt="" class="w-4 sm:w-5" />
              {{ recipe.time }}
            </span>

            <span class="inline-flex items-center gap-2">
              <img src="../assets/Images/ForkKnife.png" alt="" class="w-4 sm:w-5" />
              {{ recipe.category }}
            </span>
          </div>
        </div>

        <!-- Ads Card aligned within grid -->
        <div
          v-if="index === 4"
          class="bg-transparent flex items-center justify-center"
        >
          <img
            src="../assets/Images/RecipeImages/Ads.png"
            alt="Advertisement"
            class="rounded-lg w-full h-full object-contain sm:w-full md:w-full lg:w-full"
          />
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
import potChicken from "../assets/Images/RecipeImages/potChicken.png";
import Noodles from "../assets/Images/RecipeImages/noodles.png";

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
@media (max-width: 480px) {
  .simpleRecipeSection img {
    max-height: 220px;
  }
}
</style>
