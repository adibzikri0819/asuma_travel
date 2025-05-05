<template>
    <nav class="flex justify-between items-center px-6 py-4 bg-white shadow">
      <div class="text-blue-600 font-bold text-lg">
        Asuma Travel
      </div>
  
      <div class="flex items-center gap-6">
        <a href="#pakej" class="font-semibold text-black hover:text-blue-600">Pakej</a>
        <a href="#tentang-kami" class="font-semibold text-black hover:text-blue-600">Tentang Kami</a>
  
        <a
          href="https://wa.me/60123456789"
          target="_blank"
          class="bg-green-500 hover:bg-green-600 text-white font-bold px-5 py-2 rounded-full flex items-center gap-2 transition"
        >
          <span>Whatsapp</span>
          <svg xmlns="http://www.w3.org/2000/svg" fill="white" viewBox="0 0 24 24" class="w-5 h-5">
            <path d="M20.52 3.48A11.84 11.84 0 0012 0a12 12 0 00-9.4 19.14L0 24l5.16-2.6A12 12 0 0024 12a11.84 11.84 0 00-3.48-8.52zM12 22a9.94 9.94 0 01-5.1-1.41l-.37-.22-3.06 1.54.64-3.13-.2-.32A10 10 0 1112 22zm5.64-7.36c-.28-.14-1.63-.8-1.88-.9s-.44-.14-.62.14-.72.9-.88 1.08-.32.2-.6.06a8 8 0 01-2.4-1.5 9 9 0 01-1.64-2c-.18-.32 0-.5.14-.66.14-.14.32-.37.48-.56.16-.2.22-.34.34-.56a.58.58 0 000-.56c-.06-.14-.6-1.44-.82-2s-.44-.46-.62-.46-.34 0-.52 0a1 1 0 00-.72.34 3 3 0 00-1 2.22 5.14 5.14 0 001.1 2.54A11.24 11.24 0 0014 17a4.57 4.57 0 002.6.86 2.3 2.3 0 001.5-1.1 1.92 1.92 0 00.14-1.1c-.08-.14-.26-.2-.54-.34z" />
          </svg>
        </a>
      </div>
    </nav>

    <div class="bg-blue-700 py-12 text-center">
      <h1 class="text-white text-3xl md:text-4xl font-bold">
        Pakej Mesra Muslim 2024/2025
      </h1>
    </div>

    <section class="px-8 py-16 max-w-7xl mx-auto">
      <h2 class="text-3xl font-bold text-center text-blue-800 mb-12">
        Pakej-pakej
      </h2>
  
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
        <div
          v-for="(pkg, index) in packages"
          :key="index"
          class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition duration-300"
        >
          <img
            :src="pkg.image"
            :alt="pkg.title"
            class="w-full h-[180px] object-cover"
          />
          <div class="p-5">
            <span
              class="inline-block text-xs font-semibold text-blue-700 bg-blue-100 px-3 py-1 rounded-full mb-3"
            >
              {{ pkg.country }}
            </span>
            <h3 class="text-sm font-bold text-gray-900">
              {{ pkg.title }}
            </h3>
          </div>
        </div>
      </div>
    </section>

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

    <section class="py-16 bg-white">
      <div class="container mx-auto px-4 max-w-3xl">
        <!-- Section Title -->
        <h2 class="text-center text-2xl md:text-3xl font-bold text-blue-800 mb-10">Info Lanjut</h2>
  
        <!-- Accordion -->
        <div v-for="(item, index) in faqs" :key="index" class="border-b">
          <button
            @click="toggle(index)"
            class="w-full text-left py-4 px-4 bg-gray-100 hover:bg-gray-200 flex justify-between items-center focus:outline-none"
          >
            <span class="font-medium text-gray-900">{{ item.question }}</span>
            <svg
              :class="isOpen(index) ? 'rotate-180' : ''"
              class="w-5 h-5 transition-transform duration-300"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div v-if="isOpen(index)" class="px-4 pb-4 text-gray-700 text-sm">
            {{ item.answer }}
          </div>
        </div>
      </div>
    </section>

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

import { ref } from 'vue'

const packages = [
  {
    country: 'Japan',
    title: 'Tokyo 5D4N',
    image: '/images/tokyo.jpg',
  },
  {
    country: 'Japan',
    title: 'Osaka Kyoto 5D4N',
    image: '/images/osaka.jpg',
  },
  {
    country: 'Japan',
    title: 'Hokkaido 5D4N',
    image: '/images/hokkaido.jpg',
  },
  {
    country: 'Maldives',
    title: 'Maldives 3D2N',
    image: '/images/maldives1.jpg',
  },
  {
    country: 'Maldives',
    title: 'Maldives 4D3N',
    image: '/images/maldives2.jpg',
  },
  {
    country: 'Vietnam',
    title: 'Ho Chi Minh - Dalat - Muine 4D3N',
    image: '/images/vietnam1.jpg',
  },
  {
    country: 'Vietnam',
    title: 'Ho Chi Minh 4D3N',
    image: '/images/vietnam2.jpg',
  },
  {
    country: 'Korea',
    title: 'Seoul 6D4N',
    image: '/images/seoul.jpg',
  },
]

// Example icons (replace with your actual SVGs or components)
const IconLightbulb = () => h('div', '💡')
const IconHalalAccess = () => h('div', '🕌')
const IconMeal = () => h('div', '🍽️')
const IconCalendar = () => h('div', '🗓️')

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

  const activeIndex = ref(null)
  
  const toggle = (index) => {
    activeIndex.value = activeIndex.value === index ? null : index
  }
  
  const isOpen = (index) => {
    return activeIndex.value === index
  }
  
  const faqs = [
    {
      question: 'What is Muslim-friendly travel?',
      answer:
        'Muslim-friendly travel refers to travel experiences that cater specifically to the needs and preferences of Muslim travelers. This includes ensuring access to halal food, prayer facilities, and activities that align with Islamic values, allowing travelers to enjoy their trips without compromising their faith.',
    },
    {
      question: 'How do you ensure halal meals during trips?',
      answer:
        'We partner with halal-certified restaurants and ensure that all meals provided meet halal standards during the trip.',
    },
    {
      question: 'Are your tours designed with prayer facilities in mind?',
      answer:
        'Yes, we schedule regular prayer breaks and ensure access to prayer facilities throughout our tours.',
    },
    {
      question: 'Can I customize my travel itinerary?',
      answer:
        'Absolutely! We offer customizable packages to cater to your specific needs and preferences.',
    },
    {
      question: 'Are your tours family-friendly?',
      answer:
        'Yes, our tours are designed to be inclusive and enjoyable for travelers of all ages, including families.',
    },
    {
      question: 'What if I have special dietary requirements?',
      answer:
        'We can accommodate most dietary needs. Just let us know in advance and we’ll take care of it!',
    },
  ]
</script>



