<template>
  <section class="px-5 md:px-10 py-10">
    <div
      class="subScribe text-center rounded-2xl flex justify-center items-center min-h-[60vh] bg-cover bg-no-repeat bg-center"
    >
      <div class="w-full max-w-2xl  p-6 md:p-10 rounded-2xl">
        <h2 class="text-2xl md:text-4xl font-semibold mb-4">
          Deliciousness to your inbox
        </h2>
        <p class="text-gray-700 text-sm md:text-base mb-6">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </p>

        <div
          class="flex flex-col sm:flex-row items-center justify-center bg-white rounded-lg shadow-md overflow-hidden"
        >
          <input
            type="text"
            placeholder="Enter your email address"
            class="px-4 py-3 w-full sm:w-auto flex-grow border-0 focus:outline-none text-sm"
          />
          <button
            class="bg-black text-white px-6 py-3 text-sm md:text-base w-full sm:w-auto hover:bg-gray-800 transition-all"
          >
            Subscribe
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.subScribe {
  background: url('../assets/Images/subscribeBg.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
