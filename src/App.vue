<template>
  <div class="container">
    <Header />
    <HeroSection />
    <Values />
    <Producers />
    <Delivery />
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import Values from './components/Values.vue'
import Producers from './components/Producers.vue'
import Delivery from './components/Delivery.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  font-family: var(--font-primary);
  color: var(--text-color);
  background-color: var(--background-color);
  position: relative;
}
</style>
