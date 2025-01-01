<template>
    <nav class=" top-0 left-0 right-0 bg-white z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16 items-center">
          <!-- Logo -->
          <div class="flex items-center">
            <span class="text-3xl font-bold text-black">Slick</span>
          </div>
  
          <!-- Desktop Navigation -->
          <div class="hidden md:flex items-center space-x-8">
            <a href="#" class="text-lg font-medium text-gray-800 hover:text-gray-600">Home</a>
            <a href="#" class="text-lg font-medium text-gray-800 hover:text-gray-600">Shop</a>
            <a href="#" class="text-lg font-medium text-gray-800 hover:text-gray-600">Collection</a>
            <a href="#" class="text-lg font-medium text-gray-800 hover:text-gray-600">Customize</a>
          </div>
  
          <!-- Action Buttons & Mobile Menu Icon -->
          <div class="flex items-center space-x-4">
            <!-- Search Button -->
            <button class="p-2 hover:bg-gray-100 rounded-full">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
              </svg>
            </button>
  
            <!-- Cart Button -->
            <button class="p-2 hover:bg-gray-100 rounded-full">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
              </svg>
            </button>
  
            <!-- Mobile Menu Toggle -->
            <button @click="toggleMobileMenu" class="p-2 hover:bg-gray-100 rounded-full">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              </svg>
            </button>
          </div>
        </div>
  
        <!-- Mobile Menu -->
        <div v-if="isMobileMenuOpen" class=" mt-2 bg-gray shadow-lg rounded-lg">
          <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Home</a>
          <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Shop</a>
          <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Collection</a>
          <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Customize</a>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: "Navbar",
    data() {
      return {
        isMobileMenuOpen: false,
      };
    },
    methods: {
      toggleMobileMenu() {
        this.isMobileMenuOpen = !this.isMobileMenuOpen;
      },
    },
  };
  </script>
  
  <style>
  /* Add any additional global styles if needed */
  </style>
  