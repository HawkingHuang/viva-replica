<script setup>
import { Swiper, SwiperSlide } from "swiper/vue"
import "swiper/css"
import "swiper/css/navigation"
import { Navigation } from "swiper/modules"

const banners1 = [
  { img: "/public/images/ED0246E39278668AE05400144FF82309_m.webp" },
  { img: "/public/images/E8C55FAAC07266AFE05400144FF9CEC6_m.jpg" },
  { img: "/public/images/28F6F18C84B50A16E06400144FF9CEC6_m.jpg" },
  { img: "/public/images/E8C55FAAC07366AFE05400144FF9CEC6_m.jpg" },
  { img: "/public/images/28F6E5D6FA700284E06400144FF9CEC6_m.jpg" },
  { img: "/public/images/E8D5482DDCC22157E05400144FF9CEC6_m.jpg" },
  { img: "/public/images/E8C60E933122296DE05400144FF9CEC6_m.webp" },
  { img: "/public/images/E8C580515EF163F1E05400144FF82309_m.webp" },
  { img: "/public/images/28F6E54C571A0444E06400144FF9CEC6_m.jpg" },
  { img: "/public/images/27E14FA13217560BE06400144FF82309_m.jpg" },
  { img: "/public/images/E8C55FAAC08966AFE05400144FF9CEC6_m.webp" },
  { img: "/public/images/E8C580515EEE63F1E05400144FF82309_m.webp" },
  { img: "/public/images/ED06AA0FAB706686E05400144FF82309_m.webp" },
  { img: "/public/images/EE10ED5F4A03009EE05400144FF9CEC6_m.webp" },
  { img: "/public/images/E8C580515EF263F1E05400144FF82309_m.webp" },
  { img: "/public/images/E8C580515EF063F1E05400144FF82309_m.webp" }
]
</script>

<template>
  <div>
    <div class="h-[46px] bg-[#3f3c42]">
      <div class="container-xl flex justify-between items-center px-2 mx-auto">
        <div class="flex items-center">
          <button class="h-[46px]"><img src="/public/images/viva-logo-white.png" class="h-[32px]"></button>
          <button class="h-[46px] pl-6"><img src="/public/images/logo-right-gif.png" class="h-[46px]"></button>
        </div>
        <div class="flex items-center">
          <div class="text-white p-2"><button><i class="bi bi-cart"></i> 購物車</button></div>
          <div class="text-white p-2"><button><i class="bi bi-person"></i> 會員專區</button></div>
          <div class="text-white p-2"><button><i class="bi bi-box-arrow-in-right"></i> 登入</button></div>
        </div>
      </div>
    </div>

    <div class="container-xl grid grid-cols-8 py-4 gap-4">
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/F5E2973B615C3EECE05400144FF82309_m.webp" class="w-[132px] rounded-full">
        旗艦館總覽
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/27B6DACBF1D53F30E06400144FF82309_m.jpg" class="w-[132px] rounded-full">
        悅讀美好
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/260FA1A01D375CF8E06400144FF9CEC6_m.jpg" class="w-[132px] rounded-full">
        本月優惠精選
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/F6092A72CB3E2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        品味生活
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/F6092A72CB3F2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        質感家電
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/F6092A72CB402D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        時尚名品
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/F6092A72CB5A2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        健康生活
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/public/images/F6092A72CB5B2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        美味食光
      </div>
    </div>

    <div class="container-xl py-12">
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="8"
        :slides-per-group="8" 
        :space-between="10"
        :navigation="true"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container"
      >
        <SwiperSlide v-for="(banner, index) in banners1" :key="index">
          <img :src="banner.img" :alt="banner.alt" class="banner-image" />
        </SwiperSlide>
      </Swiper>
    </div>
  </div>
</template>

<style scoped>
:deep(.swiper-button-prev),
:deep(.swiper-button-next) {
  width: 36px;
  height: 72px;
  background: white !important;
  border-radius: 36px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease-in-out, transform 0.3s ease-in-out;
  z-index: 50;
}

:deep(.swiper-button-prev)::after,
:deep(.swiper-button-next)::after {
  font-size: 20px;
  color: #333 !important;
}

:deep(.swiper-button-prev),
.swiper-container:not(:hover) :deep(.swiper-button-prev) {
  transform: translateX(30px);
}

:deep(.swiper-button-next),
.swiper-container:not(:hover) :deep(.swiper-button-next) {
  transform: translateX(-30px);
}

.swiper-container:hover :deep(.swiper-button-prev) {
  opacity: 1;
  transform: translateX(-5px);
}

.swiper-container:hover :deep(.swiper-button-next) {
  opacity: 1;
  transform: translateX(5px);
}
</style>