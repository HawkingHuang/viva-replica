<script setup>
import Header from './components/Header.vue'
import Upper from './components/Upper.vue'
import Lower from './components/Lower.vue'
import Misc from './components/Misc.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>
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
</template>

<style scoped>
.main {
  background: url('/images/background_repeat.png');
  background-size: 100% auto, 100% auto;
}
</style>