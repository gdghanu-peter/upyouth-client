<template>
    <div class="mt-16 px-20 py-20">
      <div class="text-center w-full inline-block px-6 py-3 rounded-md border-2 border-blue-700">
      <h2 class="text-3xl font-bold text-blue-700 pb-3">Co-Founders</h2>
    </div>

      <div class="mt-12">
        <div class="flex flex-wrap justify-center gap-32">
          <div v-for="(founder, item) in founders" :key="item" class="flex flex-col items-center">
            <img :src="founder.image" alt="Chair Photo" class="w-40 h-40 object-cover rounded-full mb-4" />
            <h4 class="text-lg font-bold text-blue-500 transition-colors duration-300 ease-in-out hover:text-blue-700">{{ founder.name }}</h4>
            <p class="text-md text-gray-500 font-semibold text-center whitespace-nowrap" v-html="founder.position"></p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  const founders = ref([
    {
      image: '/co-founder1.png',
      name: 'Mr. Brian Minh Tran',
      position: '- Forbes 30U30 Asia <br/>- Ex-Assistant to VinFast Global DCEO',
      image: '/co-founder1.png'
    },
    {
      name: 'Mr. Nam Doan',   
      position: '- Accelerator Program Manager at <br/>ThinkZone Ventures',
      image: '/co-founder2.png'
    }
  ]);
  </script>
  
