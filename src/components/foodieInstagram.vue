<template>
  <section class="bg-[#eafafd] px-5 py-5 md:px-10 md:py-15">
    <h2 class="md:text-4xl text-3xl text-center font-[600] md:mb-5">Check out @foodieland on Instagram</h2>
    <p class="md:w-170 text-center mx-auto">Lorem ipsum dolor sit amet, consectetuipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqut enim ad minim</p>

    <div class="flex flex-col md:flex-row gap-10 mt-10 mb-10">
      <div v-for="post in posts" :key="post.id" class="bg-white">
        <div class="flex items-center gap-10 mb-5 bg-white p-2">
          <div class="flex gap-3 items-center">
            <img src="../assets/Images/InstagramImages/Oval.png" alt class="w-8 h-8" />
            <div>
              <strong class="flex gap-3 mb-0">
                Foodieland
                <img src="../assets/Images/InstagramImages/Official Icon.png" class="w-5 h-5" alt />
              </strong>
              <span>Tokyo, Japan</span>
            </div>
          </div>

          <div>
            <img src="../assets/Images/InstagramImages/More Icon.png" alt />
          </div>
        </div>
        <div class="relative">
          <img :src="post.image" alt class="h-[300px] object-cover" />
          <span
            class="bg-[#4d4f50] text-white absolute px-3 py-1 rounded-full top-5 right-3"
          >{{ post.number }}</span>
        </div>
        <div class="p-2">
          <div class="flex justify-between items-center mb-3">
            <div class="flex gap-2">
              <img src="../assets/Images/InstagramImages/Like.png" alt />
              <img src="../assets/Images/InstagramImages/Comment.png" alt />
              <img src="../assets/Images/InstagramImages/Messanger.png" alt />
            </div>

            <div>
              <img src="../assets/Images/InstagramImages/Pagination.png" alt />
            </div>

            <div>
              <img src="../assets/Images/InstagramImages/Save.png" alt />
            </div>
          </div>

          <div class="flex gap-2">
            <img src="../assets/Images/InstagramImages/instagrammer.png" alt="" class="w-5 h-4">
            <p class="text-[10px]">
              Liked by
              <b>craig_love</b> and
              <b>44,686</b>
            </p>
          </div>
          <p class="text-[10px]">
            <b>Foodieland.</b>
            {{ post.content }}
          </p>
        </div>
      </div>
    </div>

    <div class="text-center mt-5">
    <router-link to="" class="bg-black text-white px-4 py-2 rounded-xl">View on Instagram </router-link>
    </div>
  </section>
</template>

<script setup>
import image1 from "../assets/Images/InstagramImages/Rectangle.png";
import image2 from "../assets/Images/InstagramImages/Rectangle (1).png";
import image3 from "../assets/Images/InstagramImages/Rectangle (2).png";
import image4 from "../assets/Images/InstagramImages/Rectangle (3).png";
const posts = [
  {
    id: 1,
    image: image1,
    content:
      "The vegetables dishes need to have certain vitamin for those people",
    number: "1/4"
  },

  {
    id: 2,
    image: image2,
    content:
      "Sweet food can bring someon into happiness as long as they don’t eat to much",
    number: "2/4"
  },

  {
    id: 3,
    image: image3,
    content:
      "What are you doing before start cooking? prepare the  tools or ingredients?",
    number: "3/4"
  },

  {
    id: 4,
    image: image4,
    content:
      "Foodieland. Steak never be wrong, it’s suitable for you who want romantic dinner",
    number: "4/4"
  }
];
</script>

<style scoped>
</style>
