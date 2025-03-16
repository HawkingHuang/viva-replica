<script setup>
import { Swiper, SwiperSlide } from "swiper/vue"
import "swiper/css"
import { Navigation, Pagination } from "swiper/modules"
import "swiper/css/navigation"
import 'swiper/css/pagination'

const top = [
  {
    img: "/images/1 (25).jpg",
    title: "ROYAL DIAMOND石墨烯美型褲",
    price: "2990"
  },
  {
    img: "/images/1 (26).jpg",
    title: "Nashihada極效紫草奇肌舒緩膏(15ml/盒)x6盒",
    price: "1663"
  },
  {
    img: "/images/1 (27).jpg",
    title: "U-Link生命之花量子共振心經鍊",
    price: "9900"
  },
  {
    img: "/images/1 (28).jpg",
    title: "奔馳醋酸銅遠紅外線醫療襪(6雙)",
    price: "2970"
  },
  {
    img: "/images/1 (29).jpg",
    title: "穆拉德幅護成6盒(30粒/盒)×6盒",
    price: "1888"
  },
  {
    img: "/images/2.jpg",
    title: "黃金週特惠! 諾得挪威85%rTG高濃度魚油(30粒/盒)×8盒",
    price: "2980"
  },
  {
    img: "/images/1 (30).jpg",
    title: "Dr.Schaumann德國超能靈活霜(250g/盒)×4盒",
    price: "2970"
  },
  {
    img: "/images/1 (31).jpg",
    title: "黃金週特惠! S.MARINE 時尚多功能後背包",
    price: "1590"
  },
  {
    img: "/images/1 (32).jpg",
    title: "COACH 經典兩用水桶包VIP限定",
    price: "8316"
  },
  {
    img: "/images/1 (33).jpg",
    title: "米特克高輕抗藍光遮光大眼鏡x2",
    price: "990"
  }
]

const recommended = [
  [
    {
      img: "/images/1.webp",
      title: "【Sea of Spa】死海鹽皂 x2入",
      price: "480"
    },
    {
      img: "/images/1 (2).webp",
      title: "【SEA OF SPA】高效草本-強效舒緩保濕霜120ml",
      price: "1680"
    }
  ],
  [
    {
      img: "/images/1.jpg",
      title: "【PASCUAL帕斯特】兒童草莓優格袋裝(80G/袋) X24袋",
      price: "1089"
    },
    {
      img: "/images/1 (3).webp",
      title: "【勝崎生鮮】美國整帶雪花牛火鍋肉片8盒組(200公克/盒)",
      price: "1199"
    }
  ],
  [
    {
      img: "/images/1 (1).webp",
      title: "IF100%椰子汁350ML 24瓶",
      price: "990",
      originalPrice: "1190"
    },
    {
      img: "/images/1 (4).webp",
      title: "【開運方程式】頂級烏拉圭紫晶鎮200g-470g(隨機出貨)",
      price: "1299"
    }
  ],
  [
    {
      img: "/images/1 (1).jpg",
      title: "【西華】30cm厚釜不沾炒鍋(含蓋) ASW-030JNS",
      price: "1680"
    },
    {
      img: "/images/1 (3).jpg",
      title: "《台塑生醫》Dr’s Formula 豐盈噴黑護髮素250ml",
      price: "425",
      originalPrice: "459",
      discount: "93折"
    }
  ],
  [
    {
      img: "/images/1 (2).jpg",
      title: "【咀七碗】古早味油飯(550g)x3包",
      price: "590"
    },
    {
      img: "/images/1 (5).webp",
      title: "五檔一鍵增壓止水蓮蓬頭（超值4入）RA2202-1",
      price: "680"
    }
  ],
  [
    {
      img: "/images/1 (4).jpg",
      title: "【MATRIC 松木】全電壓 600ml溫控電熱水杯MH-BT0625L",
      price: "1288",
      originalPrice: "1980",
      discount: "65折"
    },
    {
      img: "/images/1 (6).webp",
      title: "《台塑生醫》Dr’s Formula 固齒健-牙齦牙周雙護理牙膏12入",
      price: "950",
      originalPrice: "1194",
      discount: "8折"
    }
  ],
  [
    {
      img: "/images/1 (5).jpg",
      title: "【QiMart】大容量可收納可加大多功能旅行袋(B款)-2入",
      price: "436"
    },
    {
      img: "/images/1 (9).jpg",
      title: "【Korea King】Diamond X拋金盾鐵炒鍋-28公分",
      price: "1880",
      originalPrice: "3280",
      discount: "57折"
    }
  ],
  [
    {
      img: "/images/1 (6).jpg",
      title: "【M2nd】希伊瑪心形鴕鳥零錢包(綠)",
      price: "1580",
      originalPrice: "4980",
      discount: "32折"
    },
    {
      img: "/images/1 (10).jpg",
      title: "【長榮生醫】益生循環專利赤鴨配方輕體順暢5盒經濟組(3g*30包/盒)",
      price: "1844",
      originalPrice: "3480"
    }
  ],
  [
    {
      img: "/images/1 (7).jpg",
      title: "【TWLADY】多功能蒸煮蛋器/可煮5顆蛋/6槽功能/智能溫控",
      price: "1118",
      originalPrice: "2050",
      discount: "55折"
    },
    {
      img: "/images/1 (7).webp",
      title: "Flextail 迷你電動兩用充抽氣機 (Max Pump 2 Plus)",
      price: "1190"
    }
  ],
  [
    {
      img: "/images/1 (8).jpg",
      title: "【CHILL愛吃】鱈魚棒棒條(100g/包)x4包",
      price: "572"
    },
    {
      img: "/images/1 (11).jpg",
      title: "Dr.愛伊健康 活關捷專利ASU活肽舒骨靈精華(50ml/瓶)x3瓶組",
      price: "1762"
    }
  ]
]

const newItems = [
  [
    {
      img: "/images/1 (12).jpg",
      title: "【M2nd】希伊瑪心形鴕鳥零錢包 (藍)",
      price: "1,580"
    },
    {
      img: "/images/1 (13).jpg",
      title: "【Korea King】韓國製 陶瓷水妍晶緞不沾單柄湯鍋 (附鍋蓋)",
      price: "1,399"
    },
  ],
  [
    {
      img: "/images/1 (14).jpg",
      title: "SINGHA SODA WATER 勝獅氣泡礦泉水 玻璃瓶裝 325mlx2",
      price: "699"
    },
    {
      img: "/images/1 (15).jpg",
      title: "【動風】雙燈管吸入式電擊捕蚊燈/可壁掛/桌立 DHF-S2188",
      price: "1,080"
    },
  ],
  [
    {
      img: "/images/1 (16).jpg",
      title: "3M 防蟎枕心-標準型 (限量版)",
      price: "599"
    },
    {
      img: "/images/1 (17).jpg",
      title: "【西班牙帕斯特 PASCUAL】原味優格 (120GX4) /組X6組/箱",
      price: "899"
    },
  ],
  [
    {
      img: "/images/1 (8).webp",
      title: "【DOD】RXW968 1440P GPS 雙子後鏡頭立雙分割",
      price: "12,800"
    },
    {
      img: "/images/1 (18).jpg",
      title: "【SOMGEN 松井】日系 4.2KG 節能雙槽洗衣機 / 雙槽洗衣機 / 洗",
      price: "2,880"
    },
  ],
  [
    {
      img: "/images/1 (9).webp",
      title: "【佛院】釋迦牟尼佛 銅雕",
      price: "42,000"
    },
    {
      img: "/images/1 (10).webp",
      title: "【真心良品】KEYWAY 美格五開式折疊收納箱 50L - 2入",
      price: "1,380"
    },
  ],
  [
    {
      img: "/images/1 (11).webp",
      title: "【Sea of Spa】死海洋去角質沐浴露 (400ml)",
      price: "580"
    },
    {
      img: "/images/1 (19).jpg",
      title: "【M2nd】英式古典鴕鳥凱莉包 (灰)",
      price: "16,800"
    },
  ],
  [
    {
      img: "/images/1 (12).webp",
      title: "【愛國者】GODEYES M99 高畫質 1080P 無線 WIFI 傳輸防水",
      price: "5,900"
    },
    {
      img: "/images/1 (20).jpg",
      title: "長庚綜合消化酵素 2 瓶組",
      price: "1,900"
    },
  ],
  [
    {
      img: "/images/1 (21).jpg",
      title: "Kamera Ai 語音輸入 翻譯秘書 USB 麥克風 隨插即用 黑科技",
      price: "590"
    },
    {
      img: "/images/1 (22).jpg",
      title: "【好滋好液】棒棒腿造型餅乾 (50g/包) x8包",
      price: "768"
    },
  ],
  [
    {
      img: "/images/1 (23).jpg",
      title: "Kamera 歐系簡約 質感皮革防水桌墊 80x40cm - 軍綠",
      price: "390"
    },
    {
      img: "/images/1 (13).webp",
      title: "【HKIL-巾專家】蓬鬆系列卡通熊毛巾-6 入組",
      price: "630"
    },
  ],
  [
    {
      img: "/images/1 (24).jpg",
      title: "【歌林】雙截式充電三層電蚊拍 (可當手電筒) KEM-123",
      price: "399"
    },
    {
      img: "/images/1 (14).webp",
      title: "【HARIO】V60 磁石 01 無限濾杯 附愛情白鴿濾紙",
      price: "950"
    },
  ],
]
</script>

<template>
  <div class="lower">
    <div class="relative container-xl py-4">
      <h5 class="!font-bold py-2 !text-[#e60012]"><i class="bi bi-star-fill"></i> 人氣熱銷</h5>
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="1"
        :slides-per-group="1" 
        :space-between="15"
        :navigation="true"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container"
        style="position: unset;"
        :breakpoints="{
          640: {
            slidesPerView: 2,
            slidesPerGroup: 2
          },
          840: {
            slidesPerView: 3,
            slidesPerGroup: 3
          },
          1200: {
            slidesPerView: 4,
            slidesPerGroup: 4
          },
          1536: {
            slidesPerView: 5,
            slidesPerGroup: 5
          }
        }"
      >
        <SwiperSlide v-for="(item, index) in top" :key="index">
          <div class="border bg-[#fff] p-2 shadow-sm flex flex-col h-[340px]">
            <div class="w-[228px] mx-auto overflow-hidden">
              <img :src="item.img" class="w-full hover:scale-110 duration-500" />
            </div>
            <div class="flex-grow">
              <p class="pt-1 line-clamp-2 h-[48px] overflow-hidden leading-snug">
                {{ item.title }}
              </p>
            </div>
            <p class="text-red-500">${{ item.price }}</p>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="relative container-xl py-4">
      <h6 class="!font-bold py-2"><i class="bi bi-hand-thumbs-up"></i> 熱銷推薦</h6>
      <Swiper
        :modules="[Navigation, Pagination]"
        :slides-per-view="1"
        :slides-per-group="1" 
        :space-between="15"
        :navigation="true"
        :pagination="{ clickable: true }"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container"
        style="position: unset;"
        :breakpoints="{
          640: {
            slidesPerView: 2,
            slidesPerGroup: 2
          },
          840: {
            slidesPerView: 3,
            slidesPerGroup: 3
          },
          1200: {
            slidesPerView: 4,
            slidesPerGroup: 4
          },
          1536: {
            slidesPerView: 5,
            slidesPerGroup: 5
          }
        }"
      >
        <SwiperSlide v-for="(item, index) in recommended" :key="index">
          <div class="border bg-[#fff] p-2 shadow-sm flex flex-col h-[340px]">
            <div class="w-[228px] mx-auto overflow-hidden">
              <img :src="item[0].img" class="w-full hover:scale-110 duration-500" />
            </div>
            <div class="flex-grow">
              <p class="pt-1 line-clamp-2 h-[48px] overflow-hidden leading-snug">
                {{ item[0].title }}
              </p>
            </div>
            <p class="text-red-500">${{ item[0].price }}</p>
          </div>
          <div class="border bg-[#fff] p-2 shadow-sm flex flex-col h-[340px] mt-3">
            <div class="w-[228px] mx-auto overflow-hidden">
              <img :src="item[1].img" class="w-full hover:scale-110 duration-500" />
            </div>
            <div class="flex-grow">
              <p class="pt-1 line-clamp-2 h-[48px] overflow-hidden leading-snug">
                {{ item[1].title }}
              </p>
            </div>
            <p class="text-red-500">${{ item[1].price }}</p>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="relative container-xl py-4">
      <h6 class="!font-bold py-2"><i class="bi bi-box"></i> 本週新品</h6>
      <Swiper
        :modules="[Navigation, Pagination]"
        :slides-per-view="1"
        :slides-per-group="1" 
        :space-between="15"
        :navigation="true"
        :pagination="{ clickable: true }"
        autoplay="false"
        :grab-cursor="true"
        class="swiper-container"
        style="position: unset;"
        :breakpoints="{
          640: {
            slidesPerView: 2,
            slidesPerGroup: 2
          },
          840: {
            slidesPerView: 3,
            slidesPerGroup: 3
          },
          1200: {
            slidesPerView: 4,
            slidesPerGroup: 4
          },
          1536: {
            slidesPerView: 5,
            slidesPerGroup: 5
          }
        }"
      >
        <SwiperSlide v-for="(item, index) in newItems" :key="index">
          <div class="border bg-[#fff] p-2 shadow-sm flex flex-col h-[340px]">
            <div class="w-[228px] mx-auto overflow-hidden">
              <img :src="item[0].img" class="w-full hover:scale-110 duration-500" />
            </div>
            <div class="flex-grow">
              <p class="pt-1 line-clamp-2 h-[48px] overflow-hidden leading-snug">
                {{ item[0].title }}
              </p>
            </div>
            <p class="text-red-500">${{ item[0].price }}</p>
          </div>
          <div class="border bg-[#fff] p-2 shadow-sm flex flex-col h-[340px] mt-3">
            <div class="w-[228px] mx-auto overflow-hidden">
              <img :src="item[1].img" class="w-full hover:scale-110 duration-500" />
            </div>
            <div class="flex-grow">
              <p class="pt-1 line-clamp-2 h-[48px] overflow-hidden leading-snug">
                {{ item[1].title }}
              </p>
            </div>
            <p class="text-red-500">${{ item[1].price }}</p>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>
  </div>
</template>


<style scoped>
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
  background-color: gray;
  opacity: 0.5;
  border-radius: 9999px;
  transition: all 0.3s ease-in-out;
}

:deep(.swiper-pagination-bullet-active) {
  width: 18px;
  height: 6px;
  background-color: gray;
  opacity: 1;
  border-radius: 9999px;
}
</style>