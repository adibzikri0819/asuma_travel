<template>
    <footer class="bg-blue-800 text-white py-8">
      <div class="container mx-auto px-4 flex flex-col md:flex-row md:justify-between items-start md:items-center gap-6">
        <!-- Left Column -->
        <div>
          <p class="font-bold">Asuma Travel</p>
          <p class="text-sm">MOTAC L/N/11970</p>
        </div>
  
        <!-- Center Column -->
        <div>
          <p class="font-bold">Asuma Travel Sdn Bhd</p>
          <p class="text-sm">Company No : 1310173–P</p>
          <p class="text-sm">15–1A, Jalan Pandan 3/10, Pandan Jaya</p>
          <p class="text-sm">55100 Kuala Lumpur, Malaysia</p>
          <p class="text-sm">hello@jomjapan.com</p>
        </div>
  
         <!-- Right Section (Socials) -->
      <div class="flex items-center gap-6 text-xl text-white/80">
        <NuxtLink to="#" aria-label="Facebook" class="hover:text-white">
          <i class="fab fa-facebook-f"></i>
        </NuxtLink>
        <NuxtLink to="#" aria-label="Twitter" class="hover:text-white">
          <i class="fab fa-twitter"></i>
        </NuxtLink>
        <NuxtLink to="#" aria-label="Instagram" class="hover:text-white">
          <i class="fab fa-instagram"></i>
        </NuxtLink>
      </div>
      </div>
    </footer>
  </template>
  
  <script setup>
  // No script needed for static footer
  </script>
  
  <style scoped>
  /* Optional: include FontAwesome if not already available */
  </style>
  