<template>
  <section class="px-8 py-16 max-w-7xl mx-auto">
    <h2 class="text-3xl font-bold text-center text-blue-800 mb-12">
      Pakej-pakej
    </h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
      <NuxtLink
        v-for="(pkg, index) in packages"
        :key="index"
        :to="`/${pkg.country.toLowerCase()}/${pkg.slug}`" 
        class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition duration-300 block"
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
      </NuxtLink>
    </div>
  </section>
</template>

  
  <script setup>
  const packages = [
    {
      country: 'Japan',
      title: 'Tokyo 5D4N',
      image: '/images/tokyo.jpg',
      slug: 'tokyo',
    },
    {
      country: 'Japan',
      title: 'Osaka Kyoto 5D4N',
      image: '/images/osaka.jpg',
      slug: 'osaka',
    },
    {
      country: 'Japan',
      title: 'Hokkaido 5D4N',
      image: '/images/hokkaido.jpg',
      slug: 'hokkaido',
    },
    {
      country: 'Maldives',
      title: 'Maldives 3D2N',
      image: '/images/maldives1.jpg',
      slug: 'maldives3d2n',
    },
    {
      country: 'Maldives',
      title: 'Maldives 4D3N',
      image: '/images/maldives2.jpg',
      slug: 'maldives4d3n',
    },
    {
      country: 'Vietnam',
      title: 'Ho Chi Minh - Dalat - Muine 4D3N',
      image: '/images/vietnam1.jpg',
      slug: 'hochiminhdalat',
    },
    {
      country: 'Vietnam',
      title: 'Ho Chi Minh 4D3N',
      image: '/images/vietnam2.jpg',
      slug: 'hochiminh4d3n',
    },
    {
      country: 'Korea',
      title: 'Seoul 6D4N',
      image: '/images/seoul.jpg',
      slug: 'seoul',
    },
  ]
  </script>
  