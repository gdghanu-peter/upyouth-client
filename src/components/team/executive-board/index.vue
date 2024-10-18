<template>
  <div class="mt-16 px-20">
    <div class="text-center w-full inline-block px-6 py-3 rounded-md border-2 border-blue-700">
      <h2 class="text-3xl font-bold text-blue-700 pb-3">Executive Board</h2>
    </div>

    <div class="mt-8 grid gap-12">
      <Item v-for="(member, item) in executiveBoardMembers" :key="item" :member="member"
        :active-tab="activeTab[item]" @tab-click="(tab) => handleTabClick(item, tab)" />
    </div>
  </div>
</template>

<script setup lang="ts">
import Item from './item.vue';

const executiveBoardMembers = ref([
  {
    name: 'Dao Phan Anh',
    position: 'President',
    image: '/executive-board1.png',
    accomplishments: [
      '- Ex-Investments Intern at <strong>Cystic Fibrosis Foundation</strong>',
      '- Ex-Associate at <strong>LvlUp Ventures</strong> - an industry-agnostic early-stage VC',
      '- Ex-M&A Intern at <strong>KPMG</strong>. Worked on sell-side M&A insurtech and renewables transactions ($300M+ deal value)',
      '- Ex-Portfolio Manager (Tech sector) on <strong>$2M student-managed investment fund</strong>',
      '- <strong>Bermont-Carlin Scholars</strong> - top 5% finance-focused students',
      '- Finance and Business Technology major at <strong>University of Miami (3.97 GPA)</strong>',
    ],
    storyContent: 'Phan Anh can spend the whole day discussing with you about investing and building, as he believes in the virtuous cycle connecting these two factors. With a robust background in the investment sector, he has engaged in seed-stage ventures at LvlUp Ventures - Vietnam\'s largest renewable energy M&A deal, managed a $2 million student - run equity portfolio, and currently invests for a $4.5 billion foundation.He is also a real builder, shown by how he played a pivotal role in scaling a solar financing startup and builded TechYouth Incubator 2023. Now he is leading UpYouth Tech Startup Ecosystem, using his experience to connect with and bridge the gap between investors and startup builders.',
    },
{
  name: 'Pham Van Luong',
    position: 'User Growth & Development Director',
      image: '/executive-board2.png',
        accomplishments: [
          '- Financial Planning & Analysis Intern at <strong>Starbucks Vietnam</strong>',
          '- Ex-CEO Trainee at <strong>GIMO (YC W\'22)</strong>',
          '- Scholarship for Excellence (top 5% students) at <strong>National Economics University (3.90 GPA)</strong>',
        ],
          storyContent: 'Luong Pham is indeed an explorer, who is ready to wear different hats to develop her diverse background knowledge. Before becoming the Director of Growth, she spent over 2 years in the Startup Knowledge Department, delving into the realm of product building and transforming business concepts into reality. Now switching to the Growth playground, she once again combines her corporate finance expertise as a Financial Planning Analyst at Starbucks with hands-on experience working on growth strategies at GIMO, a YC W\'22 startup. Her broad understanding of both the corporate and startup ecosystems under multiple roles has made her a formiddable asset to our team. ',
    },
{
  name: 'Nguyen Canh Huy',
    position: 'Community & Partnership Director',
      image: '/executive-board3.png',
        accomplishments: [
          '- Ex-SWE Intern at <strong>Viettel Software</strong>',
          '- Ex-Quality Assurance Intern at <strong>Got It AI</strong>',
          '- First Runner-up at <strong>ICAEW Mainland China and South-East Asia Business Competition 2024',
          '- National Finalist at <strong>Cornell EMI Corning Case Competition</strong>',
          '- Honorary student at <strong>VinUni-Cornell Student Immersion Program 2023</strong>'
        ],
          storyContent: 'As a Computer Science student, Canh Huy discovered his passion for entrepreneurship after working at Got It AI Vietnam, an AI-driven startup based in Silicon Valley. He began his journey at UpYouth as a Growth Associate and quickly advanced to the role of Director of External Partnerships, developing his proficiency in strategic analysis and systemic thinking. Those skillset has made him a competent player, both in the industry and academic sectors. He got a chance to work professionally at KPMG, VinFast, and Viettel Software. At the same time, Huy made it to the final round of Cornell EMI Corning Case Competition 2024, just months after becoming the First Runner-up at the ICAEW Mainland China and South-East Asia Business Competition 2024.',
    },
  ]);

const activeTab = ref(Array(executiveBoardMembers.value.length).fill('accomplishments'));

const handleTabClick = (item: number, tab: string) => {
  activeTab.value[item] = tab;
};
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr;
}

@media (min-width: 1024px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
</style>