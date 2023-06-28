<script>
import ItemCard from '/components/ItemChart/ItemCard/ItemCard.vue';
export default {
  props: ['chartTitle', 'itemIconSeeInfo', 'timeFlashSale', 'dateLeft', 'seeMoreBtn', 'amountItemDisplay', 'dataListProduct', 'positionPrice', 'displayInline', 'smallItems'],
  components: {
    'ItemCard': ItemCard
  },
}
</script>

<style scoped></style>

<!-- <script setup>
import { defineProps } from 'vue';
import ItemCard from '/components/ItemChart/ItemCard/ItemCard.vue';
// import { Product } from '/types/product.ts'
const props = defineProps({
  chartTitle: String,
  itemIconSeeInfo: Boolean,
  timeFlashSale: Boolean,
  dateLeft: Date,
  seeMoreBtn: Boolean,
  amountItemDisplay: Number,
  // dataListProduct: [...Product],
  positionPrice: String,
  displayInline: Boolean,
  smallItems: Boolean,
  
});
</script>
<style scoped></style> -->

<template>
  <!-- COMPONENT: itemChart -->
  <section class="flex flex-col w-full">
    <!-- top-container -->
    <div class="flex w-full items-center justify-between">
      <!-- top-container left -->
      <span class="flex items-center gap-[0.5rem]">
        <!-- REQUIRED: chartTitle: sting -->
        <a href="#" :class="`font-bold ${smallItems === 'true' ? 'text-[calc(1.5rem*0.8)]' : 'text-[1.5rem]'}`">
          {{ chartTitle }}
        </a>
        <!-- REQUIRED: itemIconSeeInfo: "<svg>...</svg>" -->
        <!-- {itemIconSeeInfo} -->
        <a :class="itemIconSeeInfo === 'true' ? 'block' : 'hidden'" href=" #">
          <svg width="24" height="24" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M24 44C35.0457 44 44 35.0457 44 24C44 12.9543 35.0457 4 24 4C12.9543 4 4 12.9543 4 24C4 35.0457 12.9543 44 24 44Z"
              fill="none" stroke="#000000" stroke-width="4" stroke-linejoin="round" />
            <path d="M21 33L30 24L21 15" stroke="#000000" stroke-wid  th="4" stroke-linecap="round"
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
      </span>

      <!-- REQUIRED: seeMoreBtn: boolean-->
      <!-- if true show seeMoreBtn  -->
      <!-- else hide seeMoreBtn -->
      <a :class="seeMoreBtn === 'true' ? '' : 'hidden'" href="#" class="`text-[0.9rem]`">Xem thêm</a>

    </div>
    <!-- list items -->
    <!-- REQUIRED: {amountItemDisplay: number, dataListProduct: array} -->
    <ul :class="`flex flex-row gap-[0.9%] h-fit overflow-hidden ${displayInline === 'true' ? '' : 'flex-wrap '}`">
      <!-- map this array to each item -->
      <li v-for="product in  dataListProduct " :key="product.id"
        :style="displayInline === 'true' ? { 'min-width': `calc(100% / ${amountItemDisplay} - 0.8%)` } : { 'max-width': `calc(100% / ${amountItemDisplay} - 0.9%)`, 'margin-bottom': '1rem' }"
        class="flex ">
        <ItemCard :productData=product :positionPrice="positionPrice" :smallItems=smallItems />
      </li>
    </ul>
  </section>
</template>

