<script setup>
import { Swiper, SwiperSlide } from "swiper/vue"
import "swiper/css"
import { Navigation, Pagination, Autoplay } from "swiper/modules"
import "swiper/css/navigation"
import 'swiper/css/pagination'

const mainBanners = [
  { img: "/images/2EF485E1FFF51213E06400144FF9CEC6.jpg" },
  { img: "/images/2A3D068F67313409E06400144FF9CEC6.jpg" },
  { img: "/images/2EF4BD6781A924F7E06400144FF9CEC6.jpg" },
  { img: "/images/2DD9CB6A6C5F6986E06400144FF82309.jpg" },
  { img: "/images/2F6E2AFD66373136E06400144FF82309.jpg" },
  { img: "/images/E8C55FAAC09966AFE05400144FF9CEC6.jpg" },
  { img: "/images/2F6E2AFD66383136E06400144FF82309.jpg" },
  { img: "/images/151B603E5AD80D2DE06400144FF82309.jpg" },
  { img: "/images/2F6E2AFD66393136E06400144FF82309.jpg" }
]

const banners1 = [
  { img: "/images/ED0246E39278668AE05400144FF82309_m.webp" },
  { img: "/images/E8C55FAAC07266AFE05400144FF9CEC6_m.jpg" },
  { img: "/images/28F6F18C84B50A16E06400144FF9CEC6_m.jpg" },
  { img: "/images/E8C55FAAC07366AFE05400144FF9CEC6_m.jpg" },
  { img: "/images/28F6E5D6FA700284E06400144FF9CEC6_m.jpg" },
  { img: "/images/E8D5482DDCC22157E05400144FF9CEC6_m.jpg" },
  { img: "/images/E8C60E933122296DE05400144FF9CEC6_m.webp" },
  { img: "/images/E8C580515EF163F1E05400144FF82309_m.webp" },
  { img: "/images/28F6E54C571A0444E06400144FF9CEC6_m.jpg" },
  { img: "/images/27E14FA13217560BE06400144FF82309_m.jpg" },
  { img: "/images/E8C55FAAC08966AFE05400144FF9CEC6_m.webp" },
  { img: "/images/E8C580515EEE63F1E05400144FF82309_m.webp" },
  { img: "/images/ED06AA0FAB706686E05400144FF82309_m.webp" },
  { img: "/images/EE10ED5F4A03009EE05400144FF9CEC6_m.webp" },
  { img: "/images/E8C580515EF263F1E05400144FF82309_m.webp" },
  { img: "/images/E8C580515EF063F1E05400144FF82309_m.webp" }
]

const banners2 = [
  { img: "/images/2FF6FE6A3D26314EE06400144FF9CEC6.jpeg" },
  { img: "/images/banner.jpg" },
  { img: "/images/1475383744C53093E06400144FF82309.jpeg" },
  { img: "/images/0E7BAE9339F83C14E06400144FF9CEC6.jpeg" },
  { img: "/images/banner (1).jpg" },
  { img: "/images/banner (2).jpg" }
]
</script>

<template>
  <div class="upper">
    <div class="relative">
      <Swiper
        :modules="[Navigation, Pagination, Autoplay]"
        :slides-per-view="1"
        :space-between="0"
        :centeredSlides="true"
        :loop="true"
        :navigation="true"
        :pagination="{ clickable: true }"
        :autoplay="{ delay: 5000, disableOnInteraction: false }"
        :speed="2000"
        class="swiper-container main"
        :breakpoints="{
          1280: {
            slidesPerView: 1.8,
          }
        }"
      >
        <SwiperSlide v-for="(slide, index) in mainBanners" :key="index">
          <img :src="slide.img" class="slide-image" />
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="container-xl grid grid-cols-2 md:grid-cols-4 xl:grid-cols-8 py-4 gap-4">
      <div class="flex flex-col items-center gap-2">
        <img src="/images/F5E2973B615C3EECE05400144FF82309_m.webp" class="w-[132px] rounded-full">
        旗艦館總覽
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/27B6DACBF1D53F30E06400144FF82309_m.jpg" class="w-[132px] rounded-full">
        悅讀美好
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/260FA1A01D375CF8E06400144FF9CEC6_m.jpg" class="w-[132px] rounded-full">
        本月優惠精選
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/F6092A72CB3E2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        品味生活
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/F6092A72CB3F2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        質感家電
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/F6092A72CB402D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        時尚名品
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/F6092A72CB5A2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        健康生活
      </div>
      <div class="flex flex-col items-center gap-2">
        <img src="/images/F6092A72CB5B2D22E05400144FF82309_m.webp" class="w-[132px] rounded-full">
        美味食光
      </div>
    </div>

    <div class="relative container-xl py-4">
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="2"
        :slides-per-group="2" 
        :space-between="10"
        :navigation="true"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container"
        style="position: unset;"
        :breakpoints="{
          540: {
            slidesPerView: 3,
            slidesPerGroup: 3
          },
          768: {
            slidesPerView: 4,
            slidesPerGroup: 4
          },
          1024: {
            slidesPerView: 6,
            slidesPerGroup: 6
          },
          1536: {
            slidesPerView: 8,
            slidesPerGroup: 8
          }
        }"
      >
        <SwiperSlide v-for="(banner, index) in banners1" :key="index">
          <img :src="banner.img" :alt="banner.alt" class="banner-image" />
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="relative container-xl py-4">
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="1"
        :space-between="16"
        :loop="true"
        :navigation="true"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container"
        style="position: unset;"
        :breakpoints="{
          640: {
            slidesPerView: 2,
          },
          1024: {
            slidesPerView: 3,
          }
        }"
      >
        <SwiperSlide v-for="(banner, index) in banners2" :key="index">
          <img :src="banner.img" :alt="banner.alt" class="banner-image" />
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="container-xl py-4 grid grid-cols-1 lg:grid-cols-2 gap-2">
      <div class="shadow-sm cursor-pointer bg-white">
        <div class="relative bg-gradient-to-r from-[#800909] to-[#1e4786] text-white p-2">
          <div class="absolute inset-0 bg-[url('/images/light-sketch.png')] bg-center bg-cover"></div>
          <i class="bi bi-tv"></i> 電視購物
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-2 p-2">
          <div>
            <div class="flex gap-0.5 relative">
              <div><img src="/images/2025-03-16_194907.png" class="w-[104px] border-2 border-gray-50"></div>
              <div class="p-0.5">
                <div class="text-[#800909] inline-block border !border-[#800909] px-2 py-1">美好一台 現正播出</div>
                <p>尚品MYEZ綻耀GIA一克拉黃彩鑽</p>
                <p class="absolute bottom-0 right-0 !mb-0 text-red-500">$86,600</p>
              </div>
            </div>
            <div class="bg-[#800909] inline-block px-3 rounded-full text-white mt-1">一台節目表</div>
          </div>
          <div>
            <div class="flex gap-0.5 relative">
              <div><img src="/images/2025-03-16_194319.png" class="w-[104px] border-2 border-gray-50"></div>
              <div class="p-0.5">
                <div class="text-[#1e4786] inline-block border !border-[#1e4786] px-2 py-1">美好二台 現正播出</div>
                <p>尚品MYEZ綻耀GIA一克拉黃彩鑽</p>
                <p class="absolute bottom-0 right-0 !mb-0 text-red-500">$2,980</p>
              </div>
            </div>
            <div class="bg-[#1e4786] inline-block px-3 rounded-full text-white mt-1">二台節目表</div>
          </div>
        </div>
      </div>
      
      <div class="shadow-sm cursor-pointer hover:scale-[1.02] duration-500">
        <div class="relative bg-gradient-to-r from-[#513b2e] to-[#6f4933] text-white p-2">
          <div class="absolute inset-0 bg-[url('/images/light-sketch.png')] bg-center bg-cover"></div>
          <i class="bi bi-credit-card-2-back"></i> 刷卡優惠
        </div>
        <img src="/images/28FA9DCF48153A21E06400144FF82309_m.jpg">
      </div>
    </div>

    <div class="container-xl py-4 cursor-pointer">
      <img src="/images/16E323AC98FA4ACAE06400144FF9CEC6_m.jpg" class="mx-auto w-full max-w-[975px] hover:scale-105 duration-500">
    </div>
  </div>
</template>

<style scoped>
:deep(.main .swiper-button-prev),
:deep(.main .swiper-button-next) {
  width: 50px;
  height: 50px;
  background: #fff !important;
  border-radius: 50%;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease-in-out, transform 0.3s ease-in-out;
  z-index: 50;
  top: 50%;
  transform: translateY(-50%);
  position: absolute;
}

:deep(.main .swiper-button-prev) {
  left: 21.5%;
}

:deep(.main .swiper-button-next) {
  right: 21.5%;
}

:deep(.main:hover .swiper-button-prev),
:deep(.main:hover .swiper-button-next) {
  opacity: 1;
}


:deep(.swiper-button-prev),
:deep(.swiper-button-next) {
  width: 30px;
  height: 60px;
  background: #fff !important;
  border-radius: 30px;
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
  transform: translateX(-12px);
}

.swiper-container:hover :deep(.swiper-button-next) {
  opacity: 1;
  transform: translateX(12px);
}

:deep(.swiper-pagination) {
  padding-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 6px;
}

:deep(.swiper-pagination-bullet) {
  width: 6px;
  height: 6px;
  background-color: #fff;
  opacity: 0.5;
  border-radius: 9999px;
  transition: all 0.3s ease-in-out;
}

:deep(.swiper-pagination-bullet-active) {
  width: 18px;
  height: 6px;
  background-color: #fff;
  opacity: 1;
  border-radius: 9999px;
}

@media (max-width: 1024px) {
  :deep(.main .swiper-button-prev),
  :deep(.main .swiper-button-next),
  :deep(.swiper-button-prev),
  :deep(.swiper-button-next) {
    display: none !important;
  }
}
</style>