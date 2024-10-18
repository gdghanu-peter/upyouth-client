<template>
  <div class="relative w-screen">
    <div class="relative -mt-9 flex h-screen flex-col justify-center gap-8 lg:-mt-[112px] px-4">
      <div class="flex flex-col items-center gap-8 lg:flex-row lg:justify-center">
        <div class="flex-1 text-center">
          <div class="flex-1">
            <CommonBrandText 
              prefix="This is" 
              label="UpYouth" 
              color="blue-700"
              class="text-center text-2xl font-bold sm:text-3xl md:text-5xl lg:text-6xl" 
              background 
              slide 
            />
          </div>
          <p class="mt-1 text-base text-gray-500 sm:text-lg md:text-xl text-blue-700">
            Every member of our team cares deeply<br class="hidden sm:block" /> about technopreneurship.
          </p>
        </div>
      </div>
      <div class="text-center mt-12">
        <h2 class="text-xl font-bold sm:text-2xl md:text-4xl text-blue-700 mb-6 md:mb-10">
          We have members and alumni from <span class="text-yellow-500">ALL</span><br class="hidden sm:block" /> parts of startup ecosystem
        </h2>
        <UButton 
          label="Read our Ecosystem Reports" 
          icon="i-heroicons-arrow-right-16-solid" 
          :trailing="true" 
          variant="solid" 
          size="lg" 
          color="white" 
          class="rounded-full button-fill transition duration-200 mt-8 md:mt-10" 
          target="_blank" 
          to="https://drive.google.com/drive/folders/1fRVEc1knH6641i1rQxsi58IJ3TL7VWPI?usp=sharing" 
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>
