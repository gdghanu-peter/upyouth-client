<template>
    <div class="bg-cta mx-4 sm:mx-8 py-10 sm:py-16 text-center rounded-tl-3xl rounded-tr-3xl">
        <h1 class="text-3xl sm:text-6xl font-bold text-white mb-8" >Be a part of our can-do team.</h1>
        <div class="flex flex-col sm:flex-row px-16 gap-4 justify-center">
        <NuxtLink to="https://tally.so/r/mZzXpo" target="_blank">
          <UButton
            :ui="{ rounded: 'rounded-full' }"
            class="border-none text-primary-600 block sm:inline w-full"
            size="xl"
            color="white"
            rounded="rounded-full"
            >Join our team</UButton
          ></NuxtLink
        >
        <!-- <UButton
          class="border-white text-white block sm:inline"
          :ui="{ rounded: 'rounded-full' }"
          color="white"
          size="xl"
          variant="outline"
          >Read Reports</UButton
        > -->
      </div>
    </div>
</template>
<style scoped>
.bg-cta{
    background: conic-gradient(from -45deg at 22.03% 81.14%, rgba(7, 73, 230, 0.50) 0deg, rgba(0, 42, 143, 0.50) 360deg), conic-gradient(from 45deg at 78.8% 83.8%, #002A8F 0deg, #0749E6 360deg);
}
</style>