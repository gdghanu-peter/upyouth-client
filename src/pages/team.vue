<template>
  <div>
    <CommonHeader />
    <TeamBanner @discover="handleScrollToBanner" />
    <div ref="bannerSection">
      <TeamValue />
    </div>
    <TeamBoard />
    <TeamTrustee/>
    <TeamStory/>
    <TeamCta/>
    <CommonFooter />
  </div>
</template>

<script setup lang="ts">
const bannerSection = ref<HTMLElement | null>(null)

const handleScrollToBanner = () => {
  if (bannerSection.value) {
    bannerSection.value.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>
