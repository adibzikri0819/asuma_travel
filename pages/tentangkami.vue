<template>
    <div class="bg-blue-500 py-32 text-center">
      <h1 class="text-white text-2xl md:text-3xl font-light">Lebih dari</h1>
      <h2 class="text-white text-5xl md:text-6xl font-semibold mt-2">3000 pax</h2>
      <p class="text-white text-xl mt-2">Telah Melancong Bersama</p>
      <p class="text-white text-2xl font-medium mt-1">Asuma Travel</p>
    </div>
  
    <div class="bg-gray-400 py-20 text-center">
      <h2 class="text-white text-3xl font-medium mb-4">Jaminan Kami</h2> 
        <p class="text-white text-base">
          Kami memberikan 100% Kepuasan Untuk Pelanggan Kami
        </p>
    </div>

    <div class="py-16 px-4 md:px-20 bg-white">
  <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-6xl mx-auto">
    
    <!-- Card 1 -->
    <div class="border rounded-lg shadow p-6 text-center">
      <div class="text-5xl mb-4">
        <!-- Mosque Icon -->
        🕌
      </div>
      <h3 class="font-bold text-lg mb-2">Muslim Friendly Tour Arrangement</h3>
      <p class="text-gray-600">We have 30+ Halal food restaurant vendors & comfortable prayer place</p>
    </div>

    <!-- Card 2 -->
    <div class="border rounded-lg shadow p-6 text-center">
      <div class="text-5xl mb-4">
        <!-- Tour Guide Icon -->
        👔
      </div>
      <h3 class="font-bold text-lg mb-2">Outstanding Profesional Tour Guide</h3>
      <p class="text-gray-600">Muslim Tour Guide & fluent in 3 languages: Japanese, English, Malay</p>
    </div>

    <!-- Card 3 -->
    <div class="border rounded-lg shadow p-6 text-center">
      <div class="text-5xl mb-4">
        <!-- Car Icon -->
        🚗
      </div>
      <h3 class="font-bold text-lg mb-2">Smooth Tour</h3>
      <p class="text-gray-600">No more complain from your clients for unpleasant tour arrangement</p>
    </div>

    <!-- Card 4 -->
    <div class="border rounded-lg shadow p-6 text-center">
      <div class="text-5xl mb-4">
        <!-- Chart Icon -->
        📈
      </div>
      <h3 class="font-bold text-lg mb-2">Best Price For Value</h3>
      <p class="text-gray-600">100% In-house Tour Management. Cut middleman</p>
    </div>
    
  </div>
</div>

<div class="bg-gray-400 py-12 text-center">
    <p class="text-white text-xl mt-2">Looking to expand your package to Japan with reliable partners?</p>
    <p class="text-white text-2xl font-semibold mt-2">This is how we are going to help you</p>
    </div>

    <div class="max-w-7xl mx-auto px-4 py-8 grid md:grid-cols-2 gap-6">
    <div
      v-for="(item, index) in services"
      :key="index"
      class="bg-white rounded shadow overflow-hidden border"
    >
      <img :src="item.image" alt="" class="w-full h-48 object-cover" />
      <div class="p-4 text-center">
        <h3 class="font-semibold text-lg mb-1">{{ item.title }}</h3>
        <p class="text-sm text-gray-600">{{ item.description }}</p>
      </div>
    </div>
  </div>

 
  <div class="max-w-7xl mx-auto px-4 py-8">
    <h2 class="text-xl font-bold mb-4">Maklumat Tambahan</h2>
    <div v-for="(faq, index) in faqs" :key="index" class="border-b">
      <button
        class="w-full text-left py-4 flex justify-between items-center"
        @click="toggle(index)"
      >
        <span class="font-medium">{{ faq.question }}</span>
        <svg
          :class="[
            'w-5 h-5 transform transition-transform duration-300',
            activeIndex === index ? 'rotate-180' : ''
          ]"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M19 9l-7 7-7-7" />
        </svg>
      </button>
      <div
        v-show="activeIndex === index"
        class="text-gray-600 pb-4 transition-all duration-300"
      >
        {{ faq.answer }}
      </div>
    </div>
  </div>
  


  </template>

<script setup>

import { ref } from 'vue'


const services = [
  {
    title: 'Maximize Profit',
    description:
      "Specially tailored package based on your existing clients' demography helping you maximise your profit",
    image: '/images/money.jpg',
  },
  {
    title: 'Quick Action',
    description:
      'Quotation within same day to help you close your customer faster',
    image: '/images/clock.jpg',
  },
  {
    title: 'Full Support',
    description: 'Knowledge sharing to help you sell better',
    image: '/images/support.jpg',
  },
  {
    title: 'Guest Happiness First',
    description:
      'Experienced Japanese speaking Muslim Tour Guide is provided to bring the best for your guests',
    image: '/images/tea.jpg',
  },
  {
    title: 'Peace Of Mind',
    description:
      'A comprehensive Operation Guidelines is prepared for Tour Guide to prevent any issues during the tour',
    image: '/images/kimono.jpg',
  },
  {
    title: 'Kaizen Report',
    description:
      'Activity & Improvement Report is provided after the tour done for your long term continuous improvement',
    image: '/images/kaizen.jpg',
  },
]

const activeIndex = ref(null)

const toggle = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index
}

const faqs = [
  {
    question: 'What is Muslim-friendly travel?',
    answer: 'It refers to travel services that consider Muslim needs like halal food, prayer times, and culturally respectful environments.',
  },
  {
    question: 'How do you ensure halal meals during trips?',
    answer: 'We carefully select halal-certified restaurants or those verified to follow halal practices.',
  },
  {
    question: 'Are your tours designed with prayer facilities in mind?',
    answer: 'Yes, prayer times and facilities are considered when planning each day’s itinerary.',
  },
  {
    question: 'Can I customize my travel itinerary?',
    answer: 'Absolutely! We provide customizable options based on your preferences and requirements.',
  },
  {
    question: 'Are your tours family-friendly?',
    answer: 'Yes, our tours are designed to accommodate families of all sizes and age groups.',
  },
  {
    question: 'What if I have special dietary requirements?',
    answer: 'We cater to dietary restrictions such as vegetarian, gluten-free, and allergy-friendly meals.',
  },
]
</script>
  