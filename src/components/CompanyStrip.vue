<template>
    <div class="bg-black py-6"> <!-- Reduced padding for black strip -->
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-12 items-center justify-items-center"> <!-- Increased gap -->
          <!-- Company Logos -->
          <div
            v-for="company in data.companies"
            :key="company.name"
            class="flex items-center justify-center h-24 w-24"
          >
            <img
              :src="company.image"
              :alt="company.name"
              class="h-full w-auto object-contain grayscale hover:grayscale-0 transition duration-300"
            />
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import data from '../data';
  </script>
  
  <style>
  /* Optional: Add a hover effect for logos */
  img {
    filter: grayscale(100%);
    transition: filter 0.3s ease;
  }
  
  img:hover {
    filter: grayscale(0%);
  }
  </style>
  