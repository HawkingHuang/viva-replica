<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from "swiper/vue"
import "swiper/css"
import "swiper/css/navigation"
import { Navigation } from "swiper/modules"

const activeMenu = ref('')

const menuA = ref([
  {
    name: '聯馥食品專館',
    img: '/images/C5DF6D117D7F00E9E05400144FF9CEC6.jpg',
  },
  {
    name: '【勝崎生鮮】',
    img: '/images/EDF5B2635E802429E05400144FF9CEC6.jpg',
  },
  {
    name: '亞帝芬奇',
    img: '/images/EDF5B2635CC22429E05400144FF9CEC6.jpg',
  },
  {
    name: 'de Buyer 畢耶',
    img: '/images/DF416DF3282E5107E05400144FF82309.jpg',
  },
  {
    name: 'Sabre Paris',
    img: '/images/DF3EE7E72F9E4406E05400144FF9CEC6.jpg',
  },
  {
    name: 'M2nd珍稀皮革',
    img: '/images/D04362687E5F62F1E05400144FF82309.jpg',
  },
  {
    name: '日本HARIO',
    img: '/images/C4D9ABC8A7271231E05400144FF9CEC6.jpg',
  },
  {
    name: '台塑生醫館',
    img: '/images/C5DF6D11790D00E9E05400144FF9CEC6.jpg',
  },
  {
    name: '波西米亞人',
    img: '/images/C6834CAF704164AAE05400144FF9CEC6.jpg',
  },
  {
    name: '茶寶',
    img: '/images/D548C8B385986466E05400144FF9CEC6.jpg',
  },
  {
    name: '大侑食尚生活',
    img: '/images/C4D9ABC8A6DD1231E05400144FF9CEC6.jpg',
  },
  {
    name: '3M生活',
    img: '/images/C5DF6CB624743708E05400144FF82309.jpg',
  },
  {
    name: '好好生醫&盈翠絲',
    img: '/images/118BADB7464C68E1E06400144FF82309.jpg',
  },
  {
    name: '開運方程式',
    img: '/images/C5DF6CB6381A3708E05400144FF82309.jpg',
  },
  {
    name: 'AOTTO',
    img: '/images/2DD65F7F224D2539E06400144FF82309.jpg',
  },
  {
    name: '藏寓',
    img: '/images/CC06B5DEBBD12A06E05400144FF9CEC6.jpg',
  },
])

const menuB = ref([
  "TV熱銷快搜",
  "強檔特惠活動",
  "傢俱用品",
  "床俱寢飾",
  "鍋具/配件",
  "餐廚用品",
  "咖啡用品",
  "酒杯酒器",
  "家飾佈置",
  "衛浴用品",
  "收納晾曬",
  "居家修繕",
  "文教樂器",
  "生活百貨",
  "兒童寶貝",
  "寵物毛孩",
  "品牌推薦",
  "18禁專區"
])

const menuC = ref([
  "TV熱銷商品",
  "家電強檔推薦",
  "Dyson特惠專賣",
  "季節家電",
  "廚房家電",
  "生活家電",
  "健康 / 美容家電",
  "家電品牌推薦"
])

const menuD = ref([
  "TV熱銷商品",
  "館長嚴選精品",
  "國際精品",
  "女裝",
  "男裝",
  "童裝",
  "鞋包配件",
  "鐘錶",
  "珠寶飾品",
  "珠寶品牌",
  "服飾品牌"
])

const menuE = ref([
  "TV熱銷快搜",
  "強檔特惠活動",
  "臉部保養",
  "美體香氛",
  "髮部用品",
  "流行彩妝",
  "口腔保養",
  "品牌推薦"
])

const menuF = ref([
  "TV熱銷快找",
  "樂活養生",
  "美肌/纖體",
  "保健用品",
  "醫療用品",
  "保健品牌"
])

const menuG = ref([
  "TV熱銷快找",
  "本月特惠主打",
  "甜點零食",
  "嚴選飲品",
  "民生食材/乾貨",
  "生鮮/低溫",
  "即時料理",
  "美食品牌專館"
])

const menuH = ref([
  "TV熱銷快搜",
  "館長精選",
  "個人清潔",
  "個人用品",
  "家用清潔",
  "廚房清潔",
  "衛浴清潔",
  "清潔工具",
  "品牌推薦"
])

const menuI = ref([
  "TV熱銷快搜",
  "主題強檔推薦",
  "開運配飾",
  "風水擺飾",
  "珍藏藝術",
  "神佛像/瑞獸",
  "祭祀/祈福用品",
  "品牌推薦"
])

const menuJ = ref([
  "平板/平板週邊",
  "TV熱銷快找",
  "數位週邊",
  "ZMI"
])

const menuK = ref([
  "TV熱銷快搜",
  "【英萊斯克】全家動起來 x 運動就是生活",
  "按摩舒壓",
  "運動休閒",
  "戶外露營",
  "車用品",
  "品牌推薦"
])

const menuL = ref([
  "美好新品搶先報",
  "情意暖冬 健康迎春",
  "本月優惠精選",
  "關於旅行那些事",
  "防疫專區",
  "帶上美好露營去",
  "食光麵攤",
  "咖啡精品與生活"
])
</script>
<template>
  <div @mouseleave="activeMenu = ''" class="container-xl relative hidden 2xl:grid grid-cols-12 h-[60px] items-center px-0 z-50">
    <button @mouseenter="activeMenu = 'A'" class="h-full hover:bg-[#e0dde3]">品牌旗艦館</button>
    <button @mouseenter="activeMenu = 'B'" class="h-full hover:bg-[#e0dde3]">品味生活</button>
    <button @mouseenter="activeMenu = 'C'" class="h-full hover:bg-[#e0dde3]">質感家電</button>
    <button @mouseenter="activeMenu = 'D'" class="h-full hover:bg-[#e0dde3]">時尚名品</button>
    <button @mouseenter="activeMenu = 'E'" class="h-full hover:bg-[#e0dde3]">美妝香氛</button>
    <button @mouseenter="activeMenu = 'F'" class="h-full hover:bg-[#e0dde3]">健康生活</button>
    <button @mouseenter="activeMenu = 'G'" class="h-full hover:bg-[#e0dde3]">美味食光</button>
    <button @mouseenter="activeMenu = 'H'" class="h-full hover:bg-[#e0dde3]">日用清潔</button>
    <button @mouseenter="activeMenu = 'I'" class="h-full hover:bg-[#e0dde3]">開運珍藏</button>
    <button @mouseenter="activeMenu = 'J'" class="h-full hover:bg-[#e0dde3]">3C數位</button>
    <button @mouseenter="activeMenu = 'K'" class="h-full hover:bg-[#e0dde3]">車旅休閒</button>
    <button @mouseenter="activeMenu = 'L'" class="h-full hover:bg-[#e0dde3]">活動專區</button>
    <div v-if="activeMenu === 'A'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="10"
        :slides-per-group="8" 
        :space-between="10"
        :navigation="true"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container bg-gray-50 p-4"
        style="position: unset;"
      >
        <SwiperSlide v-for="(menu, index) in menuA" :key="index">
          <div class="border bg-[#fff] shadow-sm">
            <img :src="menu.img" class="banner-image" />
            <p class="text-sm text-center pt-2 border-t border-slate-200 w-[98%] mx-auto">{{ menu.name }}</p>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>
    <div v-if="activeMenu === 'B'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuB" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'C'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuC" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'D'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuD" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'E'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuE" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'F'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuF" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'G'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuG" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'H'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuH" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'I'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuI" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'J'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuJ" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'K'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuK" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
    <div v-if="activeMenu === 'L'" class="absolute top-full left-0 container-xl bg-[#e0dde3] p-2">
      <div class="grid grid-cols-10 justify-items-center bg-white p-4">
        <div v-for="item in menuL" :key="item" class="w-[120px] text-center text-sm px-2 py-2 m-2 border cursor-pointer hover:bg-[#e0dde3] flex items-center justify-center transition-all duration-500">
          {{ item }}
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.upper {
  background-image: url('/images/background.png');
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
  transform: translateX(-20px);
}

.swiper-container:hover :deep(.swiper-button-next) {
  opacity: 1;
  transform: translateX(20px);
}
</style>