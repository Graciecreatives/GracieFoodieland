<template>
  <section class="px-10 py-5 flex flex-col md:flex-row h-[100vh]">
    <div class="w-full md:w-1/2 bg-[#E7F9FD] p-10 rounded-l-lg">
      <div>Hot Recipes</div>
      <h1>Spicy delicious chicken wings</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat eos quaerat corporis accusantium quidem eaque illum magnam ullam hic. Non!</p>
      <button>30 Minutes</button>
      <button>Chicken</button>

<div class="flex flex-col md:flex-row md:items-center md:gap-30 gap-5">
      <div class="flex items-center gap-5">
        <img src="../assets/Images/JohnSmith.png" alt class="w-12" />
        <div>
          <strong>John Smith</strong>
          <br />
          <span>15 March, 2022</span>
        </div>
      </div>

      <div>
        <router-link to="" class="">
          <div class="bg-black text-white flex py-2 items-center align-center justify-center text-sm md:px-5 md:py-3 rounded-lg w-full gap-3">
          View Recipe <img src="../assets/Images/PlayCircle.png" alt="" class="w-7 h-[25px]">
            </div>
        </router-link>
      </div>
    </div>
    </div>

    <div class="w-full md:w-1/2 h-[92vh]">
      <img src="../assets/Images/HeroImage2.png" class="backround:cover" alt="">
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>

</style>
