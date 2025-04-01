<script setup>
import Header from './components/Header.vue'
import Upper from './components/Upper.vue'
import Lower from './components/Lower.vue'
import Misc from './components/Misc.vue'
import Footer from './components/Footer.vue'
import Aside from './components/Aside.vue'
</script>

<template>
  <header class="sticky top-0 z-[1000] bg-white">
    <Header />
  </header>

  <main class="main">
    <Upper />
    <Lower />
    <Misc />
  </main>

  <footer>
    <Footer />
  </footer>

  <Aside />
</template>

<style scoped>
.main {
  background: url('/images/background_repeat.png');
  background-size: 100% auto, 100% auto;
}
</style>