<template>
    <div
      class="relative bg-[#ff8a9e] h-[450px] w-[calc(100%-4cm)] mx-auto rounded-lg shadow-lg flex items-center"
    >
      <!-- Background Text -->
      <div class="absolute bottom-[-160px] left-[60px] text-[340px] text-pink-200 font-bold opacity-10">
        Slick
      </div>
  
      <!-- Left Section with Image -->
      <div class="w-1/2 flex justify-center relative">
        <img
          src="/assets/bannerFeet.png"
          alt="Banner Feet"
          class="max-h-[740px] object-contain relative -translate-y-20 z-10"
        />
      </div>
  
      <!-- Right Section with Button, Carousel, and Slider -->
      <div class="w-1/2 pr-12 flex flex-col items-start">
        <!-- Text Section -->
        <div class="mt-8">
          <h2 class="text-5xl font-bold text-white leading-tight">
            Are you ready to
            <br />
            lead the way
          </h2>
          <p class="mt-4 text-lg text-white">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
          </p>
        </div>
  
        <!-- Explore Button -->
        <button
          class="mt-6 px-8 py-3 bg-white text-[#ff8a9e] font-semibold rounded-none hover:bg-pink-50 transition-colors"
        >
          Explore
        </button>
  
        <!-- Carousel Section -->
        <div class="mt-8 relative w-full">
          <!-- Shoe Images Container -->
          <div class="flex justify-start space-x-4">
            <img
              src="/assets/bannerShoeGroup.png"
              alt="Banner Shoe Group"
              class="w-[300px] h-auto"
            />
          </div>
  
          <!-- Dotted Slider -->
          <div class="flex space-x-2 mt-4 ml-[120px]">
            <span
              v-for="(dot, index) in 3"
              :key="index"
              :class="[
                'cursor-pointer transition-all duration-200',
                index === 1 
                  ? 'w-6 h-2 bg-white rounded-sm' 
                  : 'w-2 h-2 bg-white/70 rounded-full'
              ]"
            ></span>
          </div>
        </div>
      </div>
  
      <!-- Navigation Arrows -->
      <button
        class="absolute left-4 top-1/2 transform -translate-y-1/2 text-white/80 text-4xl font-bold hover:text-white transition-colors"
      >
        &lt;
      </button>
      <button
        class="absolute right-4 top-1/2 transform -translate-y-1/2 text-white/80 text-4xl font-bold hover:text-white transition-colors"
      >
        &gt;
      </button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentSlide: 1,
      };
    },
  };
  </script>
  
  <style scoped>
  /* Prevent any hover effects on images */
  img {
    filter: none !important;
    transition: none !important;
  }
  </style>