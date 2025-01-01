<template>
    <section class="py-16 px-4 sm:px-6 lg:px-8 bg-gray-50">
      <div class="max-w-7xl mx-auto">
        <!-- Section Title -->
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold">— Client Testimonial —</h2>
        </div>
  
        <!-- Testimonials Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div
            v-for="testimonial in testimonials"
            :key="testimonial.name"
            class="bg-gray-200 text-black shadow-lg rounded-lg p-6 flex items-center transition-transform hover:scale-105"
          >
            <!-- Testimonial Image -->
            <div class="flex-shrink-0 flex items-center justify-center w-52 h-52 overflow-hidden">
              <img
                :src="testimonial.userImage"
                :alt="testimonial.name"
                class="w-auto h-full object-cover"
                style="object-position: center;"
              />
            </div>
  
            <!-- Testimonial Content -->
            <div class="ml-8 flex flex-col justify-center">
              <h3 class="text-xl font-semibold">{{ testimonial.name }}</h3>
              <div class="flex items-center mt-2">
                <!-- Star Ratings -->
                <span
                  v-for="star in Math.floor(testimonial.rating)"
                  :key="star"
                  class="text-yellow-400 text-xl"
                >
                  ★
                </span>
                <span
                  v-if="testimonial.rating % 1 !== 0"
                  class="text-yellow-400 text-xl"
                >
                  ☆
                </span>
                <span
                  v-for="star in 5 - Math.ceil(testimonial.rating)"
                  :key="star + 5"
                  class="text-gray-300 text-xl"
                >
                  ★
                </span>
              </div>
              <p class="mt-4 text-gray-600 leading-relaxed">
                {{ testimonial.content }}
              </p>
            </div>
          </div>
        </div>
  
        <!-- Slider Dots -->
        <div class="flex justify-center mt-8 space-x-2">
          <span
            v-for="(dot, index) in 4"
            :key="index"
            class="h-2 w-2 rounded-full cursor-pointer transition-transform duration-300 bg-gray-400 hover:bg-black"
          ></span>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  // Testimonials data
  const testimonials = [
    {
      name: "Meythli Odex",
      userImage: new URL("/src/images/testimonial1.png", import.meta.url).href,
      rating: 4.5, // Includes half a star
      content:
        "Lorem Ipsum Dolor Sit Amet, Consectetur Adipisicing Elit, Sed Do Eiusmod Tempor Incididunt Ut Labore Et Dolore Magna Aliqua.",
    },
    {
      name: "Meythli Odex",
      userImage: new URL("/src/images/testimonial2.png", import.meta.url).href,
      rating: 4.8, // Includes almost a full 5-star rating
      content:
        "Lorem Ipsum Dolor Sit Amet, Consectetur Adipisicing Elit, Sed Do Eiusmod Tempor Incididunt Ut Labore Et Dolore Magna Aliqua.",
    },
  ];
  </script>
  
  <style scoped>
  /* Ensure images retain their original shape and alignment */
  .flex-shrink-0 {
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }
  
  img {
    object-fit: cover;
    object-position: center;
    filter: none !important; /* Ensure no filter is applied to alter image colors */
    transition: none !important; /* Prevent any unwanted visual effects */
  }
  </style>
  