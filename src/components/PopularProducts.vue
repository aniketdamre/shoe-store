<template>
    <section class="py-16 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <!-- Main Flex Container -->
        <div class="flex flex-wrap lg:flex-nowrap items-start gap-12">
          <!-- Header Section -->
          <div class="w-full lg:w-1/3 text-center lg:text-left space-y-4">
            <span class="text-lg text-gray-600 block">— Our Trending Shoes</span>
            <h2 class="text-3xl md:text-4xl font-bold mt-2">Most Popular Products</h2>
            <p class="text-gray-500 mt-4">
              Discover our latest trending shoes, loved by our customers for their style and comfort.
            </p>
            <!-- Explore Button -->
            <button class="bg-black text-white px-8 py-4 text-lg hover:bg-gray-900 transition-colors">
              Explore
            </button>
          </div>
  
          <!-- Product Cards Section -->
          <div class="relative w-full lg:w-2/3">
            <!-- Product Cards -->
            <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-8">
              <div
                v-for="product in data.mostPopularProducts"
                :key="product.name"
                class="bg-gray-50 rounded-lg shadow-md hover:shadow-lg transition-shadow p-6 relative flex flex-col items-center justify-between h-[380px]"
              >
                <!-- Product Image -->
                <div class="relative">
                  <img
                    :src="product.image"
                    :alt="product.name"
                    class="w-full h-56 object-contain mb-4"
                  />
                  <span
                    v-if="product.isNew"
                    class="absolute top-4 left-4 bg-red-500 text-white text-xs uppercase px-2 py-1 rounded-full"
                  >
                    New
                  </span>
                </div>
                <!-- Product Info -->
                <h3 class="font-semibold text-lg mb-2 text-center break-words w-full">{{ product.name }}</h3>
                <div class="flex justify-between items-center w-full">
                  <p class="text-lg text-gray-700">₹{{ product.price.toLocaleString() }}</p>
                  <button
                    class="bg-black text-white p-2 hover:bg-gray-900 rounded-full"
                    aria-label="Add to Cart"
                  >
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                      <path d="M7 17L17 7" />
                      <path d="M7 7h10v10" />
                    </svg>
                  </button>
                </div>
              </div>
            </div>
  
            <!-- Scroll Dots -->
            <div class="flex justify-center items-center mt-8">
              <button
                v-for="(dot, index) in 3"
                :key="index"
                class="w-3 h-3 rounded-full border-2 border-gray-400 mx-1 hover:bg-gray-400 transition-colors"
                :class="{ 'bg-gray-400': index === 0 }"
              ></button>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>

<script setup>
import data from '../data';
</script>

<style scoped>
/* Ensure all images retain their original colors */
img {
  filter: none !important;
  transition: none !important;
}
</style>
