<template>
  <section class="w-full">
    <img
      src="/images/osaka.jpg"
      alt="Osaka"
      class="w-full h-[400px] object-cover"
    />
  </section>

  <div class="sticky top-20 float-right w-full max-w-md p-6 bg-white rounded-lg shadow-lg">
  <form class="space-y-4" id="participantForm">
    <!-- Maklumat Peserta -->
    <div>
      <label class="block text-gray-700 font-semibold mb-2">Maklumat Peserta*</label>
      <div class="flex items-center space-x-2">
        <select id="title" class="border border-gray-300 rounded px-3 py-2 w-32">
          <option value="">Pilih</option>
          <option>Puan</option>
          <option>Encik</option>
          <option>Cik</option>
        </select>
        <input
          type="text"
          id="name"
          placeholder="Nama"
          class="border border-gray-300 rounded px-3 py-2 flex-1"
        />
      </div>
      <p id="errorName" class="text-red-500 text-sm mt-1 hidden">Sila isi nama peserta.</p>
    </div>

    <!-- Nombor Telefon -->
    <div>
      <input
        type="text"
        id="phone"
        placeholder="Format: 60123"
        class="border border-gray-300 rounded px-3 py-2 w-full"
      />
      <p id="errorPhone" class="text-red-500 text-sm mt-1 hidden">Sila isi nombor telefon.</p>
    </div>

    <!-- Emel -->
    <div>
      <input
        type="email"
        id="email"
        placeholder="Emel anda"
        class="border border-gray-300 rounded px-3 py-2 w-full"
      />
      <p id="errorEmail" class="text-red-500 text-sm mt-1 hidden">Sila isi emel yang sah.</p>
    </div>

    <!-- Bilangan Peserta -->
    <div>
      <label class="block text-gray-700 font-semibold mb-2">Bilangan Peserta*</label>
      <div class="grid grid-cols-2 gap-3">
        <div>
          <label class="text-sm text-gray-600">Dewasa (>12 thn)</label>
          <input
            type="number"
            id="adult"
            value="2"
            class="border border-gray-300 rounded px-3 py-2 w-full"
          />
        </div>
        <div>
          <label class="text-sm text-gray-600">Kanak² (4-12 thn)</label>
          <input
            type="number"
            id="child"
            value="0"
            class="border border-gray-300 rounded px-3 py-2 w-full"
          />
        </div>
        <div>
          <label class="text-sm text-gray-600">Kanak² tanpa katil (2-4 thn)</label>
          <input
            type="number"
            id="toddler"
            value="0"
            class="border border-gray-300 rounded px-3 py-2 w-full"
          />
        </div>
        <div>
          <label class="text-sm text-gray-600">Bayi (≤2 thn)</label>
          <input
            type="number"
            id="infant"
            value="0"
            class="border border-gray-300 rounded px-3 py-2 w-full"
          />
        </div>
      </div>
    </div>

    <!-- Tiket Penerbangan -->
    <div class="flex items-center space-x-2">
      <input type="checkbox" id="ticket" class="border-gray-300" />
      <label for="ticket" class="text-gray-700">Sudah ada tiket penerbangan</label>
    </div>

    <!-- Maklumat Tambahan -->
    <div>
      <textarea
        rows="3"
        id="additionalInfo"
        placeholder="Maklumat tambahan"
        class="border border-gray-300 rounded px-3 py-2 w-full"
      ></textarea>
    </div>

    <!-- Submit button -->
    <div>
      <button
        type="button"
        onclick="submitForm()"
        class="w-full bg-green-500 hover:bg-green-600 text-white font-semibold py-3 rounded flex items-center justify-center space-x-2"
      >
        <span>Whatsapp</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12 0C5.372 0 0 5.373 0 12c0 2.11.547 4.09 1.508 5.817L0 24l6.377-1.668C8.03 23.451 9.964 24 12 24c6.628 0 12-5.372 12-12S18.628 0 12 0zm6.293 17.293c-.229.646-1.346 1.27-1.869 1.345-.473.067-1.078.095-1.729-.109a15.31 15.31 0 01-2.454-1.179 13.544 13.544 0 01-2.83-2.43c-.782-.88-1.526-1.84-2.148-2.91-.59-1.015-1.024-2.01-1.295-3.004-.234-.869-.155-1.529.249-2.014.398-.48 1.117-.73 1.625-.602.274.07.567.34.899.878.315.51.707 1.35.79 1.575.17.43.014.846-.293 1.13-.163.15-.335.32-.489.49-.23.26-.48.52-.45.933.033.452.277.894.753 1.418.672.72 1.279 1.396 2.049 1.916.8.543 1.469.678 2.034.404.27-.13.871-.418 1.167-.635.297-.216.656-.26.977-.13.312.124 1.963.925 2.291 1.091.338.17.564.26.645.405.08.144.08.826-.148 1.473z"/>
        </svg>
      </button>
    </div>
  </form>
</div>
  
  <div class="max-w-4xl mx-auto bg-white p-6 rounded-md space-y-6">
    <!-- Header -->
    <div>
      <span class="bg-gray-200 text-gray-600 text-xs px-2 py-1 rounded-full">Japan</span>
      <h2 class="text-xl font-semibold mt-2">Osaka Kyoto 5D4N</h2>
      <p class="text-sm text-gray-700 mt-2">
        Pakej percutian 5 hari 4 malam ke Osaka dan Kyoto ini direka khas untuk pelancong Muslim. Anda akan melawat destinasi menarik seperti Istana Nijo, Kinkakuji, Arashiyama, Fushimi Inari Taisha, dan Universal Studios Japan. Pakej ini termasuk penginapan di hotel mesra Muslim, pengangkutan persendirian, pemandu pelancong berbahasa Melayu, dan kebanyakan makanan halal. Nikmati keindahan budaya dan alam semula jadi Jepun dalam suasana yang selesa dan selamat.
      </p>
    </div>

    <!-- Divider -->
    <hr>

    <!-- Details -->
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 text-sm text-gray-800">
      <div class="flex items-start gap-3">
        <i class="fas fa-map-marker-alt text-gray-600 mt-1"></i>
        <div>
          <p class="font-semibold">Lokasi</p>
          <p>Osaka, Jepun</p>
        </div>
      </div>

      <div class="flex items-start gap-3">
        <i class="fas fa-hotel text-gray-600 mt-1"></i>
        <div>
          <p class="font-semibold">Penginapan</p>
          <p>5 hari 4 malam, 3-Star hotel atau berasrama</p>
        </div>
      </div>

      <div class="flex items-start gap-3">
        <i class="fas fa-utensils text-gray-600 mt-1"></i>
        <div>
          <p class="font-semibold">Makanan</p>
          <p>3 × sarapan makanan halal</p>
        </div>
      </div>

      <div class="flex items-start gap-3">
        <i class="fas fa-bus text-gray-600 mt-1"></i>
        <div>
          <p class="font-semibold">Pengangkutan</p>
          <p>Pengangkutan peribadi, boat</p>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <hr>

    <!-- Lokasi Map + Info -->
    <div>
      <h3 class="text-xl font-semibold mb-3">Lokasi</h3>

      <!-- Embedded Google Map -->
      <div class="overflow-hidden rounded-md mb-4">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4147.647764366413!2d135.50126420909374!3d34.69373732035519!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6000e0ddf085c02d%3A0x5c63c4d4a1e88b6c!2sOsaka%2C%20Japan!5e0!3m2!1sen!2smy!4v1615370188464!5m2!1sen!2smy"
          width="100%"
          height="250"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>

      <!-- Info Cards -->
      <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 text-sm">
        <div class="bg-gray-100 rounded-md p-3 flex flex-col items-center text-center">
          <p class="font-medium">Musim</p>
          <p class="text-gray-700">Bunga</p>
        </div>
        <div class="bg-gray-100 rounded-md p-3 flex flex-col items-center text-center">
          <p class="font-medium">Suhu</p>
          <p class="text-gray-700">20°C – 26°C</p>
        </div>
        <div class="bg-gray-100 rounded-md p-3 flex flex-col items-center text-center">
          <p class="font-medium">Matawang</p>
          <p class="text-gray-700">Yen</p>
        </div>
        <div class="bg-gray-100 rounded-md p-3 flex flex-col items-center text-center">
          <p class="font-medium">7h</p>
          <p class="text-gray-700">KUL → NRT</p>
        </div>
      </div>
    </div>

    <section class="pt-6 max-w-7xl mx-auto">
    <h2 class="text-xl font-semibold mt-2 mb-6">
      Tempat² Menarik
    </h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      <div
        v-for="(place, index) in attractions"
        :key="index"
        class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition duration-300"
      >
        <img
          :src="place.image"
          :alt="place.title"
          class="w-full h-[180px] object-cover"
        />
        <div class="p-5 text-center">
          <h3 class="font-semibold text-base mb-2">
            {{ place.title }}
          </h3>
          <p class="text-sm text-gray-600">
            {{ place.description }}
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="pt-0 pb-6 max-w-7xl mx-auto">
  <h2 class="text-xl font-semibold mt-2 mb-6">Foto Pelanggan</h2>
  <div class="flex space-x-4 overflow-x-auto scrollbar-thin scrollbar-thumb-gray-400 scrollbar-track-gray-200 pb-2">
    <div
      v-for="(place, index) in places"
      :key="index"
      class="flex-shrink-0 w-80"
    >
      <img
        :src="place.image"
        :alt="place.title"
        class="w-full h-[180px] object-cover rounded-lg shadow"
      />
    </div>
  </div>
</section>

<section class="pt-0 max-w-7xl mx-auto">
  <h2 class="text-xl font-semibold mt-2 mb-6">Review</h2>
  <div class="flex space-x-4 overflow-x-auto scrollbar-thin scrollbar-thumb-gray-400 scrollbar-track-gray-200 pb-2">
    <div
      v-for="(review, index) in reviews"
      :key="index"
      class="flex-shrink-0 w-80"
    >
      <img
        :src="review.image"
        :alt="review.title"
        class="w-full h-[180px] object-cover rounded-lg shadow"
      />
    </div>
  </div>
</section>

<section class="pt-0 max-w-7xl mx-auto">
    <h2 class="text-2xl font-bold mb-6">Jadual Perjalanan</h2>

    <div v-for="(day, index) in itinerary" :key="index" class="mb-4 rounded border overflow-hidden">
      <!-- Day Header -->
      <div class="bg-gray-200 px-4 py-2 font-semibold">
        {{ day.title }}
      </div>
      <!-- Day Activities -->
      <ul class="bg-white px-4 py-3 list-disc list-inside space-y-2">
        <li v-for="(activity, idx) in day.activities" :key="idx">
          {{ activity }}
        </li>
      </ul>
    </div>
  </section>

  <section class="max-w-5xl mx-auto p-6">
    <!-- Pakej Termasuk -->
    <div class="mb-12">
      <h2 class="text-2xl font-bold mb-6">Pakej Termasuk</h2>
      <div class="grid md:grid-cols-2 gap-8">
        <!-- Tour to sites -->
        <div>
          <div class="flex items-center gap-3 mb-2">
            <i class="fas fa-map-marker-alt text-gray-600 w-6 h-6"></i>
            <h3 class="text-lg font-semibold">Tour to sites</h3>
          </div>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Half-day Tokyo city tour base on seat-in-coach.</li>
            <li>Full-day Mt Fuji tour with lunch base on seat-in-coach.</li>
          </ul>
        </div>

        <!-- Meals -->
        <div>
          <div class="flex items-center gap-3 mb-2">
            <i class="fas fa-utensils text-gray-600 w-6 h-6"></i>
            <h3 class="text-lg font-semibold">Meals</h3>
          </div>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>4x Breakfast</li>
            <li>1x Lunch</li>
          </ul>
        </div>

        <!-- Tour Leader -->
        <div>
          <div class="flex items-center gap-3 mb-2">
            <i class="fas fa-user-tie text-gray-600 w-6 h-6"></i>
            <h3 class="text-lg font-semibold">Tour Leader</h3>
          </div>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Return to Haneda airport by seat-in-coach.</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Pakej Tidak Termasuk -->
    <div>
      <h2 class="text-2xl font-bold mb-6">Pakej Tidak Termasuk</h2>
      <div class="grid md:grid-cols-2 gap-8">
        <!-- Expenses -->
        <div>
          <div class="flex items-center gap-3 mb-2">
            <i class="fas fa-money-bill-wave text-gray-600 w-6 h-6"></i>
            <h3 class="text-lg font-semibold">Expenses</h3>
          </div>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Return flight tickets.</li>
            <li>Travel insurance/takaful.</li>
            <li>Personal expenses such as laundry, phone, room service or extra food in the hotel.</li>
          </ul>
        </div>

        <!-- Additional Tours -->
        <div>
          <div class="flex items-center gap-3 mb-2">
            <i class="fas fa-map text-gray-600 w-6 h-6"></i>
            <h3 class="text-lg font-semibold">Tour to sites</h3>
          </div>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Additional tour not mentioned inside the itinerary.</li>
            <li>Tours are weather and time dependent, may be subject to cancellations.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
  
  <section class="max-w-5xl mx-auto p-6">
    <h2 class="text-2xl font-bold mb-6">Harga</h2>

    <div class="overflow-x-auto">
      <table class="min-w-full bg-white border border-gray-200 rounded-lg overflow-hidden">
        <thead class="bg-gray-100">
          <tr>
            <th class="px-4 py-3 text-left text-sm font-semibold text-gray-700">Pax</th>
            <th class="px-4 py-3 text-left text-sm font-semibold text-gray-700">Dewasa<br/>(12 tahun ke atas)</th>
            <th class="px-4 py-3 text-left text-sm font-semibold text-gray-700">Kanak*<br/>(4 - 12 tahun)</th>
            <th class="px-4 py-3 text-left text-sm font-semibold text-gray-700">Kanak tanpa katil<br/>(2 - 4 tahun)</th>
            <th class="px-4 py-3 text-left text-sm font-semibold text-gray-700">Bayi<br/>(2 tahun ke bawah)</th>
          </tr>
        </thead>
        <tbody class="text-gray-700">
          <tr class="border-t">
            <td class="px-4 py-3">1</td>
            <td class="px-4 py-3">RM 2,400</td>
            <td class="px-4 py-3">RM 1,900</td>
            <td class="px-4 py-3">RM 1,600</td>
            <td class="px-4 py-3">RM 500</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-3">2</td>
            <td class="px-4 py-3">RM 2,400</td>
            <td class="px-4 py-3">RM 1,900</td>
            <td class="px-4 py-3">RM 1,600</td>
            <td class="px-4 py-3">RM 500</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-3">3-5</td>
            <td class="px-4 py-3">RM 2,400</td>
            <td class="px-4 py-3">RM 1,900</td>
            <td class="px-4 py-3">RM 1,600</td>
            <td class="px-4 py-3">RM 500</td>
          </tr>
          <tr class="border-t">
            <td class="px-4 py-3">6-10</td>
            <td class="px-4 py-3">RM 2,400</td>
            <td class="px-4 py-3">RM 1,900</td>
            <td class="px-4 py-3">RM 1,600</td>
            <td class="px-4 py-3">RM 500</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
  
  <section class="max-w-5xl mx-auto p-6">
    <h2 class="text-2xl font-bold mb-6">Maklumat Tambahan</h2>

    <div class="space-y-4">
      <div v-for="(item, index) in faqs" :key="index" class="border-b">
        <button
          @click="toggle(index)"
          class="w-full text-left flex justify-between items-center py-4 focus:outline-none"
        >
          <span class="font-medium">{{ item.question }}</span>
          <svg
            :class="{'transform rotate-180': activeIndex === index}"
            class="w-5 h-5 transition-transform duration-300"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M19 9l-7 7-7-7">
            </path>
          </svg>
        </button>
        <div v-if="activeIndex === index" class="pb-4 text-gray-700">
          {{ item.answer }}
        </div>
      </div>
    </div>
  </section>

  

  </div>


  
  

  
</template>

<script setup>

import { ref } from 'vue'

const activeIndex = ref(0)

const attractions = [
  {
    title: 'Osaka Castle',
    image: '/images/osaka-castle.jpg',
    description: 'Explore the historic castle grounds and enjoy panoramic city views from the top floors.'
  },
  {
    title: 'Dotonbori',
    image: '/images/dotonbori.jpg',
    description: 'Immerse yourself in the lively atmosphere, neon lights, and delicious street food of this famous entertainment district.'
  },
  {
    title: 'Universal Studios Japan',
    image: '/images/universal-studios.jpg',
    description: 'Experience thrilling rides and attractions based on popular movies and franchises like Harry Potter and Super Mario.'
  },
  {
    title: 'Umeda Sky Building',
    image: '/images/umeda.jpg',
    description: 'Marvel at the stunning city skyline from the observation deck of this architectural masterpiece.'
  },
  {
    title: 'Kuromon Market',
    image: '/images/kuromon.jpg',
    description: 'Indulge in a wide variety of fresh seafood, produce, and local delicacies at this bustling marketplace.'
  },
  {
    title: 'Osaka Aquarium Kaiyukan',
    image: '/images/kaiyukan.jpg',
    description: 'Marvel at the diverse marine life and impressive whale shark exhibit at one of the largest aquariums in the world.'
  },
  {
    title: 'Shitennoji Temple',
    image: '/images/shitennoji-temple.jpg',
    description: "Visit one of Japan's oldest temples, known for its beautiful gardens and pagoda."
  },
  {
    title: 'Namba Parks',
    image: '/images/namba-parks.jpg',
    description: "Shop and dine in this unique multi-level shopping complex with a rooftop garden."
  }
]

const places = [
  {
    title: 'Foto Pelanggan 1',
    image: '/images/holiday1.jpg',
  },
  {
    title: 'Foto Pelanggan 2',
    image: '/images/holiday2.jpg',
  },
  {
    title: 'Foto Pelanggan 3',
    image: '/images/holiday3.jpg',
  },
]

const reviews = [
  {
    title: 'Tokyo/Osaka Review One',
    image: '/images/tokyo-osaka-review-one.jpg',
  },
  {
    title: 'Tokyo/Osaka Review One',
    image: '/images/tokyo-osaka-review-one.jpg',
  },
  {
    title: 'Tokyo/Osaka Review One',
    image: '/images/tokyo-osaka-review-one.jpg',
  },
]

const itinerary = [
  {
    title: 'Day 1 - KL - Osaka (Morning Arrival)',
    activities: [
      'Arrival & Briefing from Guide',
      'Depart to Osaka Castle (The most famous castle and the remnants of the Japanese warlords)',
    ],
  },
  {
    title: 'Day 2 - Kobe',
    activities: [
      'Depart To Kobe (A city west of Osaka, see Osaka bay from the highest point of Kobe)',
      'Kobe Earthquake Disaster Reduction Institute (A memorial institute for the 1995 Great Hanshin Earthquake. Some structures are left as it is from 1995)',
    ],
  },
  {
    title: 'Day 3 - Nara - Kyoto',
    activities: [
      'Depart to Nara (A city east of Osaka. Once the capital of Japan for 74 years during the Nara period)',
      'Nara Deer Park (Stroll the park with wild deers. Be careful, do not feed them papers)',
    ],
  },
  {
    title: 'Day 4 - Free & Easy without Tour Guide',
    activities: [
      'Optional Universal Studio Japan (USJ)',
      'Price From JPY 8600~',
    ],
  },
  {
    title: 'Day 5 - Kansai Airport - KL',
    activities: [
      'Check out',
      'Depart to KL',
    ],
  },
]

const faqs = [
  {
    question: "What is Muslim-friendly travel?",
    answer: "Muslim-friendly travel refers to travel experiences that cater specifically to the needs and preferences of Muslim travelers. This includes ensuring access to halal food, prayer facilities, and activities that align with Islamic values, allowing travelers to enjoy their trips without compromising their faith."
  },
  {
    question: "How do you ensure halal meals during trips?",
    answer: "We carefully select restaurants and catering services that offer certified halal meals."
  },
  {
    question: "Are your tours designed with prayer facilities in mind?",
    answer: "Yes, we plan itineraries with easy access to mosques or prayer rooms where possible."
  },
  {
    question: "Can I customize my travel itinerary?",
    answer: "Absolutely! We can tailor the itinerary according to your preferences and requirements."
  },
  {
    question: "Are your tours family-friendly?",
    answer: "Yes, we offer tours suitable for travelers of all ages, including activities for children."
  },
  {
    question: "What if I have special dietary requirements?",
    answer: "Please inform us in advance, and we will do our best to accommodate your dietary needs."
  },
]

const toggle = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index
}

function submitForm() {
  const name = document.getElementById('name').value.trim();
  const phone = document.getElementById('phone').value.trim();
  const email = document.getElementById('email').value.trim();
  const adult = document.getElementById('adult').value.trim();
  const ticket = document.getElementById('ticket').checked ? "Sudah ada tiket" : "Belum ada tiket";
  const additionalInfo = document.getElementById('additionalInfo').value.trim();
  const title = document.getElementById('title').value.trim();

  // Reset all errors
  document.getElementById('errorName').classList.add('hidden');
  document.getElementById('errorPhone').classList.add('hidden');
  document.getElementById('errorEmail').classList.add('hidden');

  let isValid = true;

  if (name === '') {
    document.getElementById('errorName').classList.remove('hidden');
    isValid = false;
  }
  if (phone === '' || !/^60\d{8,9}$/.test(phone)) {
    document.getElementById('errorPhone').classList.remove('hidden');
    isValid = false;
  }
  if (email === '' || !/\S+@\S+\.\S+/.test(email)) {
    document.getElementById('errorEmail').classList.remove('hidden');
    isValid = false;
  }

  if (!isValid) {
    return;
  }

  // Create WhatsApp message
  const message = `Pendaftaran Peserta:
👤 Nama: ${title} ${name}
📞 Telefon: ${phone}
📧 Emel: ${email}
👨‍👩‍👧‍👦 Dewasa: ${adult}
✈️ Tiket Penerbangan: ${ticket}
📝 Maklumat Tambahan: ${additionalInfo}`;

  const encodedMessage = encodeURIComponent(message);

  // Open WhatsApp
  window.open(`https://wa.me/60183694950?text=${encodedMessage}`, '_blank');
}
</script>
