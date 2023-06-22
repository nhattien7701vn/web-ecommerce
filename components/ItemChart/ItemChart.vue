<template>
  <!-- COMPONENT: itemChart -->
  <section class="flex flex-col w-full h-full">
    <!-- top-container -->
    <div class="flex w-full items-center justify-between">
      <!-- top-container left -->
      <div class="flex items-center gap-[0.5rem]">
        <!-- REQUIRED: chartTitle: sting -->
        <a href="#" class="font-bold text-[1.5rem]">{{ chartTitle }}</a>
        <!-- REQUIRED: itemIconSeeInfo: "<svg>...</svg>" -->
        <!-- {itemIconSeeInfo} -->
        <a :class="itemIconSeeInfo === 'true' ? 'block' : 'hidden'" href=" #">
          <svg width="24" height="24" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M24 44C35.0457 44 44 35.0457 44 24C44 12.9543 35.0457 4 24 4C12.9543 4 4 12.9543 4 24C4 35.0457 12.9543 44 24 44Z"
              fill="none" stroke="#000000" stroke-width="4" stroke-linejoin="round" />
            <path d="M21 33L30 24L21 15" stroke="#000000" stroke-width="4" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </a>
        <!-- REQUIRED: timeFlashSale: boolean-->
        <!-- if true show flash sale  -->
        <!-- else hide flash sale -->
        <!-- count down timer  -->
        <ul :class="['flex', 'h-[24px]', 'gap-[4px]', 'text-[#ffffff]', timeFlashSale === 'true' ? '' : 'hidden']">
          <!-- REQUIRED: dateLeft: Date-->

          <!-- {flashSaleDayLeft} -->
          <li class="flex justify-center items-center w-[24px] text-[12px] rounded-full bg-[#000000]">21D</li>
          <li class="text-[#000000]">:</li>
          <!-- {flashSaleHourLeft} -->
          <li class="flex justify-center items-center w-[24px] text-[12px] rounded-full bg-[#000000]">7</li>
          <li class="text-[#000000]">:</li>
          <!-- {flashSaleMinuteLeft} -->
          <li class="flex justify-center items-center w-[24px] text-[12px] rounded-full bg-[#000000]">39</li>
          <li class="text-[#000000]">:</li>
          <!-- {flashSaleSecondLeft} -->
          <li class="flex justify-center items-center w-[24px] text-[12px] rounded-full bg-[#000000]">51</li>
        </ul>
      </div>

      <!-- REQUIRED: seeMoreBtn: boolean-->
      <!-- if true show seeMoreBtn  -->
      <!-- else hide seeMoreBtn -->
      <a :class="seeMoreBtn === 'true' ? '' : 'hidden'" href="#" class="text-[0.9rem]">Xem thêm</a>
    </div>
    <!-- list items -->
    <!-- REQUIRED: {amountItemInLine: number, dataListItem: array} -->
    <ul class="flex flex-row flex-wrap gap-[0.8rem]">
      <!-- map this array to each item -->
      <!-- this <li> has flex-basis=calc(100%/{amountItemInLine}-gap*{amountItemInLine}) -->
      <!-- map this array to each item -->
      <li :style="{ flexBasis: `calc(100% / ${amountItemInLine} - 0.7rem)` }" class="flex">
        <ItemCard :itemPrice="itemPrice" :imgItemSrc="imgItemSrc" />
      </li>
    </ul>
  </section>
</template>

<script>
import ItemCard from '/components/ItemChart/ItemCard/ItemCard.vue';
export default {
  props: ['chartTitle', 'itemIconSeeInfo', 'timeFlashSale', 'dateLeft', 'seeMoreBtn', 'amountItemInLine', 'dataListItem', 'imgItemSrc', 'itemPrice', 'positionPrice'],
  components: {
    'ItemCard': ItemCard
  },
}
</script>

<style scoped></style>