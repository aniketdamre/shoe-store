<template>
  <div class="min-h-screen bg-white">
    <Navbar />
    <main>
      <Hero />
      <CompanyStrip />
      <PopularProducts />
      <LeadBanner />
      <BestSelling />
      <Testimonials />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import CompanyStrip from './components/CompanyStrip.vue';
import PopularProducts from './components/PopularProducts.vue';
import LeadBanner from './components/LeadBanner.vue';
import BestSelling from './components/BestSelling.vue';
import Testimonials from './components/Testimonials.vue';
import Footer from './components/Footer.vue';
</script>