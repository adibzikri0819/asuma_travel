<template>
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
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
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
  