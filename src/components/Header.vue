<script setup>
import { ref } from 'vue'
import Dropdown from './Dropdown.vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap'
const showTwoRows = ref(false)

const toggleRows = () => {
  showTwoRows.value = !showTwoRows.value
}
</script>
<template>
  <div>
    <div class="h-[50px] 2xl:h-[46px] bg-[#3f3c42]">
      <div class="container-xl flex justify-between items-center px-2 mx-auto">
        <div class="flex items-center">
          <button class="h-[46px]"><img src="/images/viva-logo-white.png" class="h-[32px]"></button>
          <button class="h-[46px] pl-6"><img src="/images/logo-right-gif.png" class="h-[46px]"></button>
        </div>
        <div class="hidden 2xl:flex items-center gap-4">
          <div class="text-white p-2"><button><i class="bi bi-cart"></i> 購物車</button></div>
          <div class="text-white p-2"><button><i class="bi bi-person"></i> 會員專區</button></div>
          <div class="text-white p-2"><button><i class="bi bi-box-arrow-in-right"></i> 登入</button></div>
        </div>
        <div class="flex 2xl:hidden items-center gap-4">
          <div class="text-white"><button><i class="bi bi-cart"></i></button></div>
          <div class="text-white"><button><i class="bi bi-search"></i></button></div>
        </div>
      </div>
    </div>

    <div class="bg-gray-50 border-b border-gray-200 hidden 2xl:block">
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
    </div>

    <Dropdown />

    <div class="2xl:hidden fixed bottom-0 left-0 w-full bg-[#3f3c42] text-white z-50 h-[40px]">
      <div class="grid grid-cols-2 !items-center h-full">
        <button><i class="bi bi-person"></i> 會員專區</button>
        <button data-bs-toggle="offcanvas" data-bs-target="#mobileMenu"><i class="bi bi-list"></i> 選單</button>
      </div>
    </div>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="mobileMenu">
      <div class="offcanvas-header bg-[#e0dde3]">
        <h5 class="offcanvas-title">入口連結</h5>
        <button type="button" class="btn-close" data-bs-dismiss="offcanvas"></button>
      </div>
      <div class="offcanvas-body flex flex-col">
        <button class="h-full hover:bg-[#e0dde3]">品牌旗艦館</button>
        <button class="h-full hover:bg-[#e0dde3]">品味生活</button>
        <button class="h-full hover:bg-[#e0dde3]">質感家電</button>
        <button class="h-full hover:bg-[#e0dde3]">時尚名品</button>
        <button class="h-full hover:bg-[#e0dde3]">美妝香氛</button>
        <button class="h-full hover:bg-[#e0dde3]">健康生活</button>
        <button class="h-full hover:bg-[#e0dde3]">美味食光</button>
        <button class="h-full hover:bg-[#e0dde3]">日用清潔</button>
        <button class="h-full hover:bg-[#e0dde3]">開運珍藏</button>
        <button class="h-full hover:bg-[#e0dde3]">3C數位</button>
        <button class="h-full hover:bg-[#e0dde3]">車旅休閒</button>
        <button class="h-full hover:bg-[#e0dde3]">活動專區</button>
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