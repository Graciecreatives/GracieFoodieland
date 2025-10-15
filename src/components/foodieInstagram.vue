<template>
  <section class="bg-[#eafafd] px-5 py-10 md:px-10 lg:px-20">
    <!-- Header -->
    <div class="max-w-3xl mx-auto text-center">
      <h2 class="text-2xl sm:text-3xl md:text-4xl font-semibold mb-3 md:mb-5">
        Check out @foodieland on Instagram
      </h2>
      <p class="text-gray-600 text-sm sm:text-base">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </div>

    <!-- Instagram posts -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 mt-10 mb-10">
      <div
        v-for="post in posts"
        :key="post.id"
        class="bg-white rounded-xl shadow-sm hover:shadow-md transition-all duration-300"
      >
        <!-- Header section -->
        <div class="flex items-center justify-between mb-2 bg-white p-3 border-b">
          <div class="flex items-center gap-3">
            <img src="../assets/Images/InstagramImages/Oval.png" alt="Profile" class="w-8 h-8 rounded-full" />
            <div>
              <strong class="flex items-center gap-2 text-sm">
                Foodieland
                <img src="../assets/Images/InstagramImages/Official Icon.png" class="w-4 h-4" alt="Verified" />
              </strong>
              <span class="text-xs text-gray-500">Tokyo, Japan</span>
            </div>
          </div>
          <img src="../assets/Images/InstagramImages/More Icon.png" alt="More" class="w-5 h-2" />
        </div>

        <!-- Image section -->
        <div class="relative">
          <img
            :src="post.image"
            alt="Instagram post"
            class="w-full h-64 sm:h-56 md:h-64 object-cover rounded-t-xl"
          />
          <span
            class="bg-[#4d4f50] text-white text-xs absolute px-3 py-1 rounded-full top-4 right-3"
          >
            {{ post.number }}
          </span>
        </div>

        <!-- Post footer -->
        <div class="p-3 text-xs sm:text-sm">
          <div class="flex justify-between items-center mb-3">
            <div class="flex gap-3 items-center">
              <img src="../assets/Images/InstagramImages/Like.png" alt="Like" class="w-4 h-4 sm:w-5 sm:h-5" />
              <img src="../assets/Images/InstagramImages/Comment.png" alt="Comment" class="w-4 h-4 sm:w-5 sm:h-5" />
              <img src="../assets/Images/InstagramImages/Messanger.png" alt="Share" class="w-4 h-4 sm:w-5 sm:h-5" />
            </div>

            <img src="../assets/Images/InstagramImages/Pagination.png" alt="Pagination" class="hidden sm:block w-6" />

            <img src="../assets/Images/InstagramImages/Save.png" alt="Save" class="w-4 h-4 sm:w-5 sm:h-5" />
          </div>

          <div class="flex gap-2 items-center mb-1">
            <img src="../assets/Images/InstagramImages/instagrammer.png" alt="Liker" class="w-4 h-4 rounded-full" />
            <p class="text-[11px] sm:text-xs">
              Liked by <b>craig_love</b> and <b>44,686 others</b>
            </p>
          </div>

          <p class="text-[11px] sm:text-xs leading-snug">
            <b>Foodieland.</b> {{ post.content }}
          </p>
        </div>
      </div>
    </div>

    <!-- Button -->
    <div class="text-center mt-5">
      <router-link
        to=""
        class="bg-black text-white text-sm sm:text-base px-5 py-2.5 rounded-xl hover:bg-gray-900 transition-colors"
      >
        View on Instagram
      </router-link>
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
    content: "The vegetable dishes need to have certain vitamins for those people",
    number: "1/4",
  },
  {
    id: 2,
    image: image2,
    content: "Sweet food can bring happiness — as long as you don’t eat too much!",
    number: "2/4",
  },
  {
    id: 3,
    image: image3,
    content: "What are you doing before cooking? Preparing the tools or ingredients?",
    number: "3/4",
  },
  {
    id: 4,
    image: image4,
    content: "Steak is never wrong — perfect for your romantic dinner night.",
    number: "4/4",
  },
];
</script>

<style scoped>
/* Optional hover scaling for posts */
@media (hover: hover) {
  .hover\:shadow-md:hover {
    transform: translateY(-3px);
  }
}
</style>
