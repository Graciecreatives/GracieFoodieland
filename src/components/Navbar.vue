<template>
  <nav class="bg-white shadow-md">
    <div class="flex justify-between items-center px-5 py-5 md:px-10">
      <!-- Logo -->
      <div>
        <router-link to="/">
          <img src="../assets/Images/Foodieland..png" alt="Logo" class="w-32" />
        </router-link>
      </div>

      <!-- Hamburger Icon (mobile only) -->
      <div class="md:hidden cursor-pointer" @click="toggleMenu">
        <svg
          v-if="!isOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M6 18L18 6M6 6l12 12" />
        </svg>
      </div>

      <!-- Navigation Links -->
      <ul
        class="hidden md:flex gap-6 font-medium text-gray-700"
      >
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/recipes">Recipes</router-link></li>
        <li><router-link to="/blog">Blog</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
        <li><router-link to="/about">About Us</router-link></li>
      </ul>

      <!-- Social Icons -->
      <div class="hidden md:flex gap-4">
        <router-link to=""><img src="../assets/Images/001-facebook.png" alt="Facebook link" /></router-link>
        <router-link to=""><img src="../assets/Images/Path.png" alt="Twitter Link" /></router-link>
        <router-link to=""><img src="../assets/Images/004-instagram.png" alt="Instagram link" /></router-link>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="isOpen"
      class="md:hidden bg-white px-5  py-3 pb-5 space-y-4 border-t"
    >
      <ul class="flex flex-col gap-4 text-gray-700 font-medium">
        <li><router-link @click="closeMenu" to="/">Home</router-link></li>
        <li><router-link @click="closeMenu" to="/recipes">Recipes</router-link></li>
        <li><router-link @click="closeMenu" to="/blog">Blog</router-link></li>
        <li><router-link @click="closeMenu" to="/contact">Contact</router-link></li>
        <li><router-link @click="closeMenu" to="/about">About Us</router-link></li>
      </ul>

      <div class="flex gap-4 pt-3 border-t">
        <router-link to=""><img src="../assets/Images/001-facebook.png" alt=""/></router-link>
        <router-link to=""><img src="../assets/Images/Path.png" alt="" /></router-link>
        <router-link to=""><img src="../assets/Images/004-instagram.png" alt=""  /></router-link>
      </div>
    </div>

    <hr />
  </nav>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};

const closeMenu = () => {
  isOpen.value = false;
};
</script>

<style scoped>
nav {
  transition: all 0.3s ease;
}
</style>
