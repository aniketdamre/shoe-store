<template>
    <section class="py-16 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <!-- Section Title -->
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold">— Best Selling —</h2>
        </div>
  
        <!-- Category Filter Buttons -->
        <div class="flex flex-wrap justify-center gap-4 mb-12">
          <button
            v-for="category in categories"
            :key="category"
            @click="selectedCategory = category.toLowerCase()"
            :class="[ 
              'px-6 py-2 rounded-md transition-colors',
              selectedCategory === category.toLowerCase()
                ? 'bg-black text-white'
                : 'border border-gray-300 hover:bg-gray-50'
            ]"
          >
            {{ category }}
          </button>
        </div>
  
        <!-- Products Grid -->
        <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-8">
          <div
            v-for="product in data.bestSellingProducts[selectedCategory]"
            :key="product.id"
            class="bg-gray-50 border border-gray-200 rounded-lg p-6 transition-transform hover:-translate-y-1 shadow hover:shadow-lg relative"
          >
            <!-- New Tag -->
            <span
              class="absolute top-4 left-0 bg-black text-white px-3 py-1 text-sm"
              style="border-top-left-radius: 0; border-bottom-left-radius: 0; border-top-right-radius: 8px; border-bottom-right-radius: 8px;"
            >
              New
            </span>
  
            <!-- Product Image -->
            <img
              :src="product.image"
              :alt="product.name"
              class="w-full h-64 object-cover rounded-lg mb-4"
            >
  
            <!-- Product Name -->
            <h3 class="font-semibold text-lg mb-2">{{ product.name }}</h3>
  
            <!-- Price and Arrow -->
            <div class="flex items-center justify-between mb-4">
              <!-- Price Section -->
              <div class="flex items-center gap-2">
                <span class="text-lg font-bold text-gray-800">
                  ₹{{ product.discountedPrice.toLocaleString() }}
                </span>
                <span
                  v-if="product.originalPrice"
                  class="text-gray-500 line-through"
                >
                  ₹{{ product.originalPrice.toLocaleString() }}
                </span>
              </div>
  
              <!-- Arrow Button -->
              <button
                class="bg-black text-white p-2 rounded-full hover:bg-gray-900 transition-transform"
                aria-label="Arrow Icon Button"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M7 17L17 7" />
                  <path d="M7 7h10v10" />
                </svg>
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import data from '../data';
  
  // Categories for filtering
  const categories = ['Man', 'Woman', 'Boy', 'Child'];
  const selectedCategory = ref('man');
  </script>
  
  <style scoped>
  /* Ensure images stay colorful */
  img {
    filter: none !important;
    transition: none !important;
  }
  </style>
  