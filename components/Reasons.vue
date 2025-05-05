<template>
    <section class="py-16 bg-white text-center">
      <div class="container mx-auto px-4">
        <!-- Section Title -->
        <h2 class="text-2xl md:text-3xl font-bold text-blue-800 mb-4">
          Sebab Apa Travel Bersama Kami?
        </h2>
        <p class="text-gray-700 max-w-3xl mx-auto mb-16">
          Pakej percutian mesra Muslim memberi tumpuan kepada orang beragama Islam yang ingin meneroka destinasi baru dan mendalami budaya yang berbeza di seluruh dunia disamping memenuhi keperluan setiap hari bersama dengan keperluan yang memuaskan seperti kemudahan makanan mesra muslim dan solat yang pada waktunya.
        </p>
  
        <!-- Subheading -->
        <h3 class="text-2xl font-bold text-blue-800 mb-12">
          Perbezaan Pakej Kami?
        </h3>
  
        <!-- Feature Cards -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
          <!-- Item 1 -->
          <div class="flex flex-col items-center">
            <div class="text-blue-600 text-5xl mb-4">
              <IconLightbulb />
            </div>
            <h4 class="font-semibold text-lg">Pengetahuan Destinasi Pakar</h4>
            <p class="text-gray-600">Penawaran Halal yang Komprehensif</p>
          </div>
  
          <!-- Item 2 -->
          <div class="flex flex-col items-center">
            <div class="text-blue-600 text-5xl mb-4">
              <IconHalalAccess />
            </div>
            <h4 class="font-semibold text-lg text-center">Akses Eksklusif kepada Perkhidmatan Halal yang Disahkan</h4>
            <p class="text-gray-600">Penawaran Halal yang Komprehensif</p>
          </div>
  
          <!-- Item 3 -->
          <div class="flex flex-col items-center">
            <div class="text-blue-600 text-5xl mb-4">
              <IconMeal />
            </div>
            <h4 class="font-semibold text-lg text-center">Kepakaran Tanpa Tandingan dalam Perjalanan Halal</h4>
            <p class="text-gray-600">Penawaran Halal yang Komprehensif</p>
          </div>
  
          <!-- Item 4 -->
          <div class="flex flex-col items-center">
            <div class="text-blue-600 text-5xl mb-4">
              <IconCalendar />
            </div>
            <h4 class="font-semibold text-lg text-center">Itinerari Peribadi yang Disesuaikan dengan Keperluan Anda</h4>
            <p class="text-gray-600">Penawaran Halal yang Komprehensif</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  // Example icons (replace with your actual SVGs or components)
  const IconLightbulb = () => h('div', '💡')
  const IconHalalAccess = () => h('div', '🕌')
  const IconMeal = () => h('div', '🍽️')
  const IconCalendar = () => h('div', '🗓️')
  </script>
  