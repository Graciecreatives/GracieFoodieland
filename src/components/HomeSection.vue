<template>
  <section
    class="px-5 md:px-10 py-10 flex flex-col md:flex-row items-center md:items-stretch gap-8 md:gap-0 bg-white overflow-hidden"
  >
    <!-- Left Section -->
    <div
      class="w-full md:w-1/2 bg-[#E7F9FD] p-6 sm:p-10 rounded-2xl md:rounded-l-2xl md:rounded-r-none flex flex-col justify-center"
    >
      <!-- Hot Recipe Label -->
      <div
        class="bg-white rounded-lg w-fit py-1 px-4 font-semibold text-sm sm:text-base mb-3 flex gap-2 items-center shadow-sm"
      >
        <img src="../assets/Images/Hot recipe.png" alt="Hot Recipe" class="w-5 h-5" />
        Hot Recipes
      </div>

      <!-- Heading -->
      <h1
        class="text-2xl sm:text-3xl md:text-5xl font-bold leading-snug mb-4 md:mb-6 max-w-md"
      >
        Spicy Delicious Chicken Wings
      </h1>

      <!-- Description -->
      <p
        class="text-gray-700 text-sm sm:text-base mb-6 md:mb-8 leading-relaxed max-w-lg"
      >
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat eos
        quaerat corporis accusantium quidem eaque illum magnam ullam hic. Non!
      </p>

      <!-- Info Buttons -->
      <div class="flex flex-wrap gap-3 mb-6">
        <button
          class="bg-[#dbedf1] border-0 px-4 py-2 rounded-lg text-sm font-medium"
        >
        <img src="../assets/Images/Timer.png" alt="Clock Icon" class="inline w-4 h-4 mr-2" />
          30 Minutes
        </button>
        <button
          class="bg-[#dbedf1] border-0 px-4 py-2 rounded-lg text-sm font-medium"
        >
        <img src="../assets/Images/ForkKnife.png" alt="Fork Icon" class="inline w-4 h-4 mr-2" />
          Chicken
        </button>
      </div>

      <!-- Author & CTA -->
      <div
        class="flex flex-col sm:flex-row sm:items-center justify-between gap-5"
      >
        <div class="flex items-center gap-4">
          <img src="../assets/Images/JohnSmith.png" alt="John Smith" class="w-12 h-12" />
          <div>
            <strong class="text-base sm:text-lg">John Smith</strong><br />
            <span class="text-gray-500 text-sm">15 March, 2022</span>
          </div>
        </div>

        <router-link to="">
          <div
            class="bg-black text-white flex items-center justify-center gap-2 sm:gap-3 px-5 py-3 rounded-lg text-sm sm:text-base hover:bg-gray-800 transition duration-300"
          >
            View Recipe
            <img
              src="../assets/Images/PlayCircle.png"
              alt="Play Icon"
              class="w-6 h-6 sm:w-7 sm:h-7"
            />
          </div>
        </router-link>
      </div>
    </div>

    <!-- Right Section (Image) -->
    <div
      class="w-full md:w-1/2 h-[320px] sm:h-[420px] md:h-auto flex items-center justify-center"
    >
      <img
        src="../assets/Images/HeroImage2.png"
        alt="Spicy chicken wings"
        class="w-full h-full object-cover rounded-2xl md:rounded-none md:rounded-r-2xl"
      />
    </div>
  </section>
</template>

<script setup></script>

<style scoped></style>
