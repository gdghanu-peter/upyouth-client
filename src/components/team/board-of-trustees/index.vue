<template>
  <div class="mt-16 px-10 py-10">
    <div class="text-center w-full inline-block px-6 py-3 rounded-md border-2 border-blue-700">
      <h2 class="text-3xl font-bold text-blue-700 pb-3">Board Of Trustees </h2>
    </div>

    <div class="mt-12">
      <h3 class="text-2xl font-bold text-blue-700 text-center mb-8">Chairs</h3>
      <div class="flex flex-wrap md:flex-nowrap justify-center gap-6 md:gap-32">
        <div v-for="(chair, index) in chairs" :key="index" class="flex flex-col items-center w-full md:w-50">
          <img :src="chair.image" alt="Chair Photo" class="w-40 h-40 object-cover rounded-full mb-4" />
          <h4 class="text-lg font-bold text-blue-500 transition-colors duration-300 ease-in-out hover:text-blue-700">{{ chair.name }}</h4>
          <p class="text-md text-gray-500 font-semibold text-center" v-html="chair.position"></p>
        </div>
      </div>
    </div>
    <div class="mt-12">
      <h3 class="text-2xl font-bold text-blue-700 text-center mb-2">Board Advisors</h3>
      <p class="text-center text-sm text-black mb-8">*Non-exhaustive list</p>
      <div class="flex flex-wrap md:flex-nowrap justify-center gap-6 md:gap-32">
        <div v-for="(advisor, item) in advisors" :key="item" class="flex flex-col items-center w-full md:w-50">
          <img :src="advisor.image" alt="Advisor Photo" class="w-40 h-40 object-cover rounded-full mb-4" />
          <h4 class="text-lg font-bold text-blue-500 transition-colors duration-300 ease-in-out hover:text-blue-700">{{ advisor.name }}</h4>
          <p class="text-md text-gray-500 font-semibold text-center" v-html="advisor.position"></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const chairs = ref([
  {
    name: 'Ms. Thanh Hoang',
    position: '<strong>Chair</strong><br/>- MBA Candidate at Harvard Business School<br/>- Incoming Consultant at McKinsey & Company <br/>- Growth and Partnership at Arrowster',
    image: '/board-chair1.png'
  },
  {
    name: 'Mr. Vu Tran',
    position: '<strong>Vice Chair</strong> <br/>- Co-founder at Productiv <br />- Ex-Investment Banking Analyst at BDA Partners <br />- Ex-Case Team Assistant at Boston Consulting Group',
    image: '/board-chair3.png'
  },
  {
    name: 'Ms. Thi Le',
    position: '<strong>Vice Chair</strong> <br/>- Executive Assistant to Group CEO at Masan Group <br/>- Ex-Legal Intern at Dentons <br />- Ex-Strategy, Deal Advisory Associate at KPMG ',
    image: '/board-chair2.png'
  }
]);

const advisors = ref([
  {
    name: 'Ms. Huong Tran',
    position: '<strong>Board Advisor</strong><br/>- Ex-Venture Partner at <br /> Monk\'s Hill Ventures',
    image: '/board-advisor2.png'
  },
  {
    name: 'Dr. Cuong Nguyen (Miro)',
    position: '<strong>Board Advisor</strong> <br/>- Global KOL & Partnership Director at VinFast <br/>- Ex-Chief Stratefy Officer at VinAI',
    image: '/board-advisor1.png'
  },
  {
    name: 'Ms. Thao Ha',
    position: '<strong>Board Advisor</strong><br/>- Venture Partner at <br /> Integra Ventures',
    image: '/board-advisor3.png'
  }
]);
</script>
