<template>
  <div class="mb-16 mx-4">
    <div class="flex flex-col items-center justify-center gap-2 md:gap-4">
      <h1 class="text-primary-700 mb-3 sm:mb-6 text-3xl sm:text-5xl font-bold">Executive Board</h1>
      <p class="mb-8 text-center text-base  sm:text-xl max-w-[700px]">
        UpYouth leadership team consists of talented and ambitious young people, who share a deep passion for startups.
      </p>
    </div>
    <div>
        <UCarousel
            :items="executiveBoard"
            v-slot="{ item }"
            :ui="{
              item: 'basis-full justify-center',
              indicators: {
                active: 'bg-primary-700',
                inactive: 'bg-gray-300',
                wrapper:
                  'absolute flex items-center justify-center gap-3 -bottom-10 inset-x-0'
              }
            }"
            indicators
          >
            <TeamBoardItem :item="item"></TeamBoardItem>
          </UCarousel>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { ExecutiveBoardItem } from '~/types/board'

const executiveBoard = ref<ExecutiveBoardItem[]>([
  {
    name: 'Dao Phan Anh',
    img: '/team/dao-phan-anh.png',
    title: 'President',
    content: [
      `Phan Anh can spend the whole day discussing with you about investing and building, as he believes in the virtuous cycle connecting these two factors. With a robust background in the investment sector, he has engaged in seed-stage ventures at LvlUp Ventures - Vietnam's largest renewable energy M&A deal, managed a $2 million student-run equity portfolio, and currently invests for a $4.5 billion foundation.`,
      `He is also a real builder, shown by how he played a pivotal role in scaling a solar financing startup and builded TechYouth Incubator 2023. Now he is leading UpYouth Tech Startup Ecosystem, using his experience to connect with and bridge the gap between investors and startup builders.`,
      `Outside of work, he enjoys boxing as school's club captain, listening to Ted Seides' Capital Allocators and Lenny's Podcast, and binging comedy-drama (most recently Succession).`
    ]
  },
  {
    name: 'Nguyen Canh Huy',
    img: '/team/nguyen-canh-huy.png',
    title: 'Community & Partership Director',
    content: [
      `Canh Huy found his interest for entrepreneurship after working at Got It AI Vietnam, an AI-driven startup based in Silicon Valley. He first joined UpYouth as a Growth Associate, then grew different skillsets and competencies to the Director role of External Partnerships department.`,
      `He cares deeply about strategic analysis and system thinking approach, fostering a can-do spirit with diverse work experience at KPMG, VinFast, and Viettel Software.`,
      `Despite majoring in Computer Science, Huy made it to the finals and was the First Runner-up at the ICAEW Mainland China and South-East Asia Business Competition 2024. He is also an experienced mentor at different aspects, such as TedX speaking contest or business competition.`
    ]
  },
  {
    name: 'Pham Van Luong',
    img: '/team/pham-van-luong.png',
    title: 'Growth Director',
    content: [
      `Luong Pham is indeed an explorer, who is ready to wear different hats to develop her diverse background knowledge. Before becoming the Director of Growth, she spent over 2 years in the Startup Knowledge Department, delving into the realm of product building and transforming business concepts into reality.`,
      `Now switching to the Growth playground, she once again combines her corporate finance expertise as a Financial Planning Analyst at Starbucks with hands-on experience working on growth strategies at GIMO, a YC W'22 startup.`,
      `Her broad understanding of both the corporate and startup ecosystems under multiple roles has made her a formiddable asset to our team.`
    ]
  }
])
</script>
