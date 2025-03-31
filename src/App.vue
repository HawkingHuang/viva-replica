<script setup>
import Header from './components/Header.vue'
import Upper from './components/Upper.vue'
import Lower from './components/Lower.vue'
import Misc from './components/Misc.vue'
import Footer from './components/Footer.vue'

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" })
}
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

  <aside class="fixed bottom-[10vh] 2xl:bottom-[45vh] right-4 z-40">
    <div class="relative">
      <img src="/images/agent-avatar.5cdde85.png" class="w-[82px] rounded-full">
      <p class="bg-[#3f3c42] text-white text-xs 2xl:text-base inline-block px-2 py-1 !mb-0 rounded-full absolute -bottom-4 right-5">客服</p>
    </div>
  </aside>
  <aside class="hidden 2xl:block fixed bottom-[4vh] right-5 z-[1500]">
    <div class="flex flex-col bg-[#3f3c42] text-white text-sm gap-2 px-2.5 py-6 rounded-[90px]">
      <button class="flex flex-col items-center">
        <i data-feather="clock" class="w-[15px] h-[15px] stroke-3"></i>
        <p>瀏覽紀錄</p>
      </button>
      <button class="flex flex-col items-center">
        <i data-feather="credit-card" class="w-[15px] h-[15px] stroke-3"></i>
        <p>刷卡優惠</p>
      </button>
      <button class="flex flex-col items-center">
        <i data-feather="file-text" class="w-[15px] h-[15px] stroke-3"></i>
        <p>訂單查詢</p>
      </button>
      <button class="flex flex-col items-center">
        <i data-feather="user" class="w-[15px] h-[15px] stroke-3"></i>
        <p>會員專區</p>
      </button>
      <button class="flex flex-col items-center" @click="scrollToTop">
        <i data-feather="chevron-up" class="w-[15px] h-[15px] stroke-3"></i>
        <p>Top</p>
      </button>
    </div>
  </aside>
</template>

<style scoped>
.main {
  background: url('/images/background_repeat.png');
  background-size: 100% auto, 100% auto;
}
</style>