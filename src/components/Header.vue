<script setup>
import { ref } from 'vue'
const showTwoRows = ref(false)

const toggleRows = () => {
  showTwoRows.value = !showTwoRows.value
}
</script>
<template>
  <div>
    <div class="h-[46px] bg-[#3f3c42]">
      <div class="container-xl flex justify-between items-center px-2 mx-auto">
        <div class="flex items-center">
          <button class="h-[46px]"><img src="/public/images/viva-logo-white.png" class="h-[32px]"></button>
          <button class="h-[46px] pl-6"><img src="/public/images/logo-right-gif.png" class="h-[46px]"></button>
        </div>
        <div class="flex items-center gap-4">
          <div class="text-white p-2"><button><i class="bi bi-cart"></i> 購物車</button></div>
          <div class="text-white p-2"><button><i class="bi bi-person"></i> 會員專區</button></div>
          <div class="text-white p-2"><button><i class="bi bi-box-arrow-in-right"></i> 登入</button></div>
        </div>
      </div>
    </div>

    <div class="bg-gray-100 border-b border-gray-200">
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
  </div>
</template>