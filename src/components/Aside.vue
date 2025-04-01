<script setup>
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" })
}
</script>

<template>
  <div>
    <aside class="fixed bottom-[9vh] 2xl:bottom-[4vh] right-4 z-40">
      <div class="relative">
        <img src="/images/agent-avatar.5cdde85.png" class="w-[60px] 2xl:w-[82px] rounded-full shadow">
        <p class="bg-[#3f3c42] text-white text-xs 2xl:text-base inline-block px-2 py-1 !mb-0 rounded-full absolute -bottom-4 right-2.5 2xl:right-5 shadow">客服</p>
      </div>
      <div class="hidden 2xl:flex flex-col bg-[#3f3c42] text-white text-sm gap-2 px-2.5 py-6 rounded-[90px] mt-4">
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
  </div>
</template>