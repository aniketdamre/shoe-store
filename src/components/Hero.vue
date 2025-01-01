<template>
    <section class="relative min-h-[80vh] flex items-center">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full">
        <div class="grid md:grid-cols-2 gap-8 items-center">
          <!-- Left Section -->
          <div class="space-y-6">
            <h1 class="text-5xl md:text-7xl font-bold leading-tight font-poppins">
              Find Your<br />
              Sole Mate<br />
              With Us
            </h1>
            <p class="text-gray-600 text-lg max-w-md">
              Lorem Ipsum Dolor Sit Amet, Consectetur Adipiscing Elit, Sed Do Eiusmod
            </p>
            <button class="bg-black text-white px-8 py-3 text-lg hover:bg-gray-900 transition-colors">
              Shop Now
            </button>
          </div>
  
          <!-- Right Section -->
          <div class="relative bg-gray-200 h-full min-h-[600px] flex items-center overflow-hidden">
            <!-- Product Container -->
            <div class="relative z-10 w-full">
              <img 
                :src="data.heroProduct.image" 
                :alt="data.heroProduct.name" 
                class="w-full max-w-xl transform -rotate-[25deg] mx-auto"
              />
              <!-- Product Details -->
              <div class="absolute bottom-4 right-36">
                <h3 class="text-2xl font-semibold">{{ data.heroProduct.name }}</h3>
                <p class="text-xl">₹ {{ data.heroProduct.price }}</p>
              </div>
            </div>
          </div>
        </div>
        <!-- Centered Vertical ULTIMATE Text -->
        <div class="absolute left-[52.5%] -translate-x-1/2 top-1/2 -translate-y-1/2 text-[130px] font-bold text-white leading-none select-none whitespace-nowrap z-0 transform -rotate-90">
          ULTIMATE
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import data from '../data';
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');
  
  .font-poppins {
    font-family: 'Poppins', sans-serif;
  }
  </style>
