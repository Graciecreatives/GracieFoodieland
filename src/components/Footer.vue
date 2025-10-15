<template>
  <footer class="bg-white">
    <div class="px-5 md:px-10 md:py-5 py-5">
      <div class="flex flex-col md:flex-row md:justify-between md:items-center gap-6 text-center md:text-left">
        <!-- Left side -->
        <div class="md:w-1/2">
          <img src="../assets/Images/Foodieland..png" alt="" class="mb-3 mx-auto md:mx-0" />
          <p class="text-gray-600 text-sm md:text-base leading-relaxed">
            Lorem ipsum dolor sit amet, consectetuipisicing elit,
          </p>
        </div>

        <!-- Social icons -->
        <div class="flex justify-center md:justify-end gap-5">
          <router-link to="">
            <img src="../assets/Images/001-facebook.png" alt=""  />
          </router-link>
          <router-link to="">
            <img src="../assets/Images/Path.png" alt="" />
          </router-link>
          <router-link to="">
            <img src="../assets/Images/004-instagram.png" alt="" />
          </router-link>
        </div>
      </div>
    </div>

    <hr class="border-gray-300" />
    <p class="text-center mt-3 mb-5 text-gray-500 text-sm md:text-base">
      &copy; {{ year }} Graciecreatives
    </p>
  </footer>
</template>

<script setup>
const year = new Date().getFullYear();
</script>

<style scoped>
footer {
  width: 100%;
}
</style>
