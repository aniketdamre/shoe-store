<template>
    <footer class="bg-black text-white py-12 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <div class="grid md:grid-cols-3 gap-8 text-center md:text-left relative">
          <!-- Column 1: Brand Information -->
          <div class="flex flex-col items-center md:items-start space-y-4">
            <h3 class="text-2xl font-bold">Slick</h3>
            <p class="text-gray-400 text-sm">
              Lorem Ipsum Dolor Sit Amet, Consectetur Adipisicing Elit, Sed Do Eiusmod Tempor Incididunt Ut Labore Et Dolore Magna Aliqua.
            </p>
            <div class="flex space-x-4">
              <a href="#" class="flex items-center justify-center w-8 h-8 bg-white text-black rounded-full hover:bg-gray-200" aria-label="Facebook">
                <i class="fab fa-facebook-f text-lg"></i>
              </a>
              <a href="#" class="flex items-center justify-center w-8 h-8 bg-white text-black rounded-full hover:bg-gray-200" aria-label="Instagram">
                <i class="fab fa-instagram text-lg"></i>
              </a>
            </div>
          </div>
  
          <!-- Column 2: Newsletter -->
          <div class="flex flex-col items-center space-y-4 md:relative md:left-6">
            <h3 class="text-lg font-bold">Subscribe to our news letter</h3>
            <form class="flex flex-col space-y-4 w-full max-w-sm">
              <input
                type="email"
                placeholder="Enter Email..."
                class="p-3 w-full rounded-md bg-white text-black text-sm mt-2"
              />
            </form>
          </div>
  
          <!-- Column 3: Quick Links -->
          <div class="flex flex-col items-center md:items-start space-y-2 absolute right-8 top-0">
            <h3 class="text-lg font-bold">Quick Link's</h3>
            <ul class="space-y-2 text-sm">
              <li><a href="#" class="text-gray-400 hover:text-white">Home</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white">Shop</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white">Collection</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white">Contact</a></li>
              <li><a href="#" class="text-gray-400 hover:text-white">Privacy</a></li>
            </ul>
          </div>
        </div>
  
        <!-- Footer Bottom -->
        <div class="mt-8 text-center text-gray-500 text-sm">
          <hr class="border-gray-700 mb-1 w-10 mx-auto" />
          <p>slick.com © all rights reserved</p>
        </div>
      </div>
    </footer>
  </template>
  
  <script setup>
  // No additional logic required
  </script>
  
  <style scoped>
  @import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css";
  
  footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  </style>
  