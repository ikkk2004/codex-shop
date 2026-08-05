<script setup>
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import IntroSection from './components/IntroSection.vue'
import MenuSection from './components/MenuSection.vue'
import VisitSection from './components/VisitSection.vue'
import SiteFooter from './components/SiteFooter.vue'
</script>

<template>
  <SiteHeader />
  <main id="top">
    <HeroSection />
    <IntroSection />
    <MenuSection />
    <VisitSection />
  </main>
  <SiteFooter />
</template>
