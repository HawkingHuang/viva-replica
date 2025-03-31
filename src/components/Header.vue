<script setup>
import { onMounted, ref, nextTick } from 'vue'
import Dropdown from './Dropdown.vue'

onMounted(() => {
  feather.replace()
})

const showTwoRows = ref(false)
const toggleRows = () => {
  showTwoRows.value = !showTwoRows.value
}

const showSideNav = ref(false)
const toggleSideNav = () => {
  showSideNav.value = !showSideNav.value
  nextTick(() => {
    feather.replace()
  })
}

const leftSideNav = ref([
  '品牌旗艦館',
  '品味生活',
  '質感家電',
  '時尚名品',
  '美妝香氛',
  '健康生活',
  '美味食光',
  '日用清潔',
  '開運珍藏',
  '3C數位',
  '車旅休閒',
  '活動專區'
])

const rightSideNav = ref([
  '聯馥食品專館',
  '【勝崎生鮮】',
  '亞帝芬奇',
  'de Buyer 畢耶',
  'Sabre Paris',
  'M2nd珍稀皮革',
  '日本HARIO',
  '台塑生醫館',
  '波西米亞人',
  '茶寶',
  '大侑食尚生活',
  '3M生活',
  '好好生醫&盈翠絲',
  '開運方程式',
  'AOTTO',
  '藏寓',
])
</script>
<template>
  <div>
    <div class="h-[46px] bg-[#3f3c42]">
      <div class="container-xl flex justify-between items-center px-2 mx-auto">
        <div class="flex items-center pl-1 xl:pl-0">
          <button class="h-[46px]"><img src="/images/viva-logo-white.png" class="h-[32px]"></button>
          <button class="h-[46px] pl-6"><img src="/images/logo-right-gif.png" class="h-[46px]"></button>
        </div>
        <nav class="hidden xl:flex items-center gap-4">
          <div class="text-white p-2">
            <button class="flex items-center gap-3">
              <div class="relative"><i data-feather="shopping-cart" class="w-[16px] h-[16px] stroke-3"></i><p class="absolute -top-2 -right-2 bg-[#e60013] text-[#fff] text-[11px] font-bold w-[15px] h-[15px] flex justify-center items-center rounded-full">0</p></div> 購物車
            </button>
          </div>
          <div class="text-white p-2">
            <button class="flex items-center gap-2">
              <div><i data-feather="user" class="w-[16px] h-[16px] stroke-3"></i></div> 會員專區
            </button>
          </div>
          <div class="text-white p-2">
            <button class="flex items-center gap-2">
              <div><i data-feather="log-in" class="w-[16px] h-[16px] stroke-3"></i></div> 登入
            </button>
          </div>

        </nav>
        <nav class="flex xl:hidden items-center gap-4">
          <div class="text-white">
            <button class="flex items-center gap-2">
              <div class="relative"><i data-feather="shopping-cart" class="w-[20px] h-[20px] stroke-3"></i><p class="absolute -top-2 -right-2 bg-[#e60013] text-[#fff] text-[11px] font-bold w-[15px] h-[15px] flex justify-center items-center rounded-full">0</p></div>
            </button>
          </div>
          <div class="text-white"><button class="flex items-center gap-2"><i data-feather="search" class="w-[20px] h-[20px] stroke-3"></i></button></div>
          <div class="text-white">
            <button class="flex items-center gap-2" @click="toggleSideNav">
              <i data-feather="menu" class="w-[20px] h-[20px] stroke-3"></i>
            </button>
          </div>
        </nav>
      </div>
    </div>

    <nav class="bg-gray-50 border-b border-gray-200 hidden 2xl:block">
      <div class="container-xl flex h-[54px] items-center">
        <div class="h-full flex flex-1 justify-start items-center gap-4">
          <div>全區最殺4折起</div>
          <div>法國艾許新品</div>
          <div>♥COACH</div>
          <div>婦樂透✪滿額贈</div>
          <div>娘家益生菌88折</div>
          <div>澳洲和牛新上市！</div>
          <div>奧利塔55折起</div>
          <div>熱銷蠶絲皂</div>
        </div>
        <div class="px-2">
          <button @click="toggleRows" v-if="showTwoRows"><i class="bi bi-chevron-up"></i></button>
          <button @click="toggleRows" v-else><i class="bi bi-chevron-down"></i></button>
        </div>
        <div class="flex">
          <input class="border rounded-tl rounded-bl px-2 py-1.5 w-[190px] placeholder-gray-600" type="text" placeholder="全站免運！搜尋商品">
          <button class="bg-[#6c757d] text-[#fff] px-3 !rounded-tr !rounded-br border-[#6c757d] block">搜尋</button>
        </div>
      </div>
      <div v-if="showTwoRows" class="container-xl flex h-[54px] items-center">
        <div class="h-full flex flex-1 justify-start items-center gap-4">
          <div>防蟎抗菌洗衣精</div>
          <div>獅王清潔48折起</div>
          <div>德恩奈買二送二</div>
        </div>
      </div>
    </nav>

    <Dropdown />

    <nav class="2xl:hidden fixed bottom-0 left-0 w-full bg-[#3f3c42] text-white z-50 h-[50px]">
      <div class="grid grid-cols-4 !items-center h-full pt-1">
        <button class="flex flex-col items-center">
          <i data-feather="clock" class="w-[15px] h-[15px] stroke-3"></i>
          <p class="text-xs !mb-0.5">瀏覽紀錄</p>
        </button>
        <button class="flex flex-col items-center">
          <i data-feather="credit-card" class="w-[15px] h-[15px] stroke-3"></i>
          <p class="text-xs !mb-0.5">刷卡優惠</p>
        </button>
        <button class="flex flex-col items-center">
          <i data-feather="file-text" class="w-[15px] h-[15px] stroke-3"></i>
          <p class="text-xs !mb-0.5">訂單查詢</p>
        </button>
        <button class="flex flex-col items-center">
          <i data-feather="user" class="w-[15px] h-[15px] stroke-3"></i>
          <p class="text-xs !mb-0.5">會員專區</p>
        </button>
      </div>
    </nav>

    <nav v-if="showSideNav" class="bg-[#3f3c42] fixed top-0 left-0 w-full z-50 h-[46px] pl-4 pr-2">
      <div class="flex justify-between h-full">
        <div class="flex items-center gap-4">
          <div class="flex items-center text-white text-base gap-1"><i data-feather="tv" class="w-[15px] h-[15px]"></i> 1台 節目表</div>
          <div class="flex items-center text-white text-base gap-1"><i data-feather="tv" class="w-[15px] h-[15px]"></i> 2台 節目表</div>
        </div>
        <button @click="showSideNav = false" class="flex items-center text-white"><i data-feather="x-square" class="w-[20px] h-[20px]"></i></button>
      </div>
    </nav>

    <div v-if="showSideNav" class="grid grid-cols-3">
      <div class="col-span-1 bg-[#f8f9fa]">
        <div class="flex flex-col border-b border-slate-200">
          <button v-for="button in leftSideNav" :key="button" class="hover:bg-[#8f849a] hover:text-[#fff] h-[50px] !text-xs md:!text-sm xl:!text-base">{{ button }}</button>
        </div>
        <div class="flex flex-col items-center">
          <div class="flex items-center h-[40px] bg-[#f8f9fa]"><i class="bi bi-line text-[22px] text-[#00c300]"></i></div>
          <div class="flex items-center h-[40px] bg-[#f8f9fa]"><i class="bi bi-facebook text-[22px] text-[#1877f2]"></i></div>
          <div class="flex items-center h-[40px] bg-[#f8f9fa]"><i class="bi bi-youtube text-[22px] text-[#ff0000]"></i></div>
        </div>
      </div>
      <div class="col-span-2 relative">
        <nav class="bg-[#5c5365] text-[#fff] !text-xs md:!text-sm xl:!text-base flex !overflow-x-auto">
          <button v-for="button in rightSideNav" :key="button" class="h-[50px] shrink-0 mx-3">{{ button }}</button>
        </nav>
        <button class="h-[50px] bg-[#5c5365] text-[#fff] !text-xs md:!text-sm xl:!text-base absolute top-0 right-0 px-2.5"><i data-feather="chevron-down" class="w-[15px] h-[15px] stroke-3"></i></button>
      </div>
    </div>
  </div>
</template>

<style scoped>
@media (max-width: 768px) {
  #mobileMenu {
    width: 50%;
  }
}
</style>