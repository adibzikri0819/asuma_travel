<template>
    <div>
      <!-- Navbar will be shown here -->
      <Navbar />
  
      <!-- NuxtPage is where the content of the current page will be rendered -->
      <NuxtPage />
  
      <!-- Footer will be shown here -->
      <Footer />
    </div>
  </template>
  
  <script setup>
  // Import Navbar and Footer components
  import Navbar from '~/components/Navbar.vue'
  import Footer from '~/components/Footer.vue'
  </script>
  