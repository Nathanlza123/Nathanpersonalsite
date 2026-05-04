<script setup lang="ts">
import HeroSection from './components/HeroSection.vue';
import AboutSection from './components/AboutSection.vue';
import PsychologySection from './components/PsychologySection.vue';
import ContactFooter from './components/ContactFooter.vue';
</script>

<template>
  <main>
    <HeroSection />
    <AboutSection />
    <PsychologySection />
    <ContactFooter />
  </main>
</template>

<style scoped>
main {
  overflow-x: hidden;
}
</style>
