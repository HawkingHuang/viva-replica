<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import { Navigation } from "swiper/modules";

const banners = [
  { img: "/public/images/2FFA73E5EC845DB2E06400144FF9CEC6_m.jpg" },
  { img: "/public/images/2DC7EE226E2237ADE06400144FF9CEC6_m.jpg" },
  { img: "/public/images/2D9C7F8320E81105E06400144FF9CEC6_m.jpg" },
  { img: "/public/images/2AC8988FD297011BE06400144FF82309_m.jpg" },
  { img: "/public/images/15E330E0A0084AE7E06400144FF82309_m.jpg" },
  { img: "/public/images/15E3285A27044AEDE06400144FF82309_m.jpg" }
];
</script>

<template>
  <div class="container-xl py-12">
    <Swiper
      :modules="[Navigation]"
      :slides-per-view="3"
      :space-between="10"
      :loop="true"
      :navigation="true"
      autoplay="false"
      :grab-cursor="true"
      class="swiper-container"
    >
      <SwiperSlide v-for="(banner, index) in banners" :key="index">
        <img :src="banner.img" :alt="banner.alt" class="banner-image" />
      </SwiperSlide>
    </Swiper>
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
