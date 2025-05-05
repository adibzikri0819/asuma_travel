<template>
    <section class="py-16 bg-gray-50 text-center">
      <div class="container mx-auto px-4">
        <!-- Section Header -->
        <h2 class="text-2xl md:text-3xl font-bold text-blue-800 mb-12">Kepakaran Kami?</h2>
  
        <!-- Grid -->
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10 place-items-center">
          <div
            v-for="(item, index) in expertiseItems"
            :key="index"
            class="flex flex-col items-center max-w-[220px]"
          >
            <div class="w-32 h-32 rounded-full overflow-hidden border-4 border-blue-700 mb-4">
              <img :src="item.image" alt="icon" class="w-full h-full object-cover" />
            </div>
            <p class="text-sm text-gray-800">{{ item.title }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const expertiseItems = [
    {
      image: '/images/halal-restaurant.jpg',
      title: 'Restoran dan makanan halal',
    },
    {
      image: '/images/recreation-men-women.jpg',
      title: 'Separate recreational areas for men and women',
    },
    {
      image: '/images/modest-dress-code.jpg',
      title: 'Modest dress code for staff',
    },
    {
      image: '/images/prayer-facility.jpg',
      title: 'Prayer facilities and qibla directions in hotels',
    },
    {
      image: '/images/alcohol-free-zone.jpg',
      title: 'Alcohol-free environments',
    },
    {
      image: '/images/sharia-finance.jpg',
      title: 'Sharia-compliant financing',
    },
  ]
  </script>
  