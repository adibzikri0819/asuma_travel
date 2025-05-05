<template>
  <nav class="flex justify-between items-center px-6 py-4 bg-white shadow">
    <NuxtLink to="/" class="text-blue-600 font-bold text-lg" >
      Asuma Travel
    </NuxtLink>

    <div class="flex items-center gap-6">
      <NuxtLink to="/pakej" class="font-semibold text-black hover:text-blue-600">
        Pakej
      </NuxtLink>
      <NuxtLink to="/tentangkami" class="font-semibold text-black hover:text-blue-600">
        Tentang Kami
      </NuxtLink>

      <a
        href="https://wa.me/60183694950"
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
</template>

<script setup>
console.log('Navbar rendered')
</script>