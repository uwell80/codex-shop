<template>
  <SiteHeader />
  <main>
    <HeroSection />
    <ManifestoSection />
    <DishesSection />
    <SpaceSection />
    <ReserveSection />
  </main>
  <SiteFooter />
</template>

<script setup>
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ManifestoSection from './components/ManifestoSection.vue'
import DishesSection from './components/DishesSection.vue'
import SpaceSection from './components/SpaceSection.vue'
import ReserveSection from './components/ReserveSection.vue'
import SiteFooter from './components/SiteFooter.vue'
</script>
