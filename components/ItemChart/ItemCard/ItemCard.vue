<template>
  <!-- component items  -->
  <!-- REQUIRED: {imgItemSrc: string, itemPrice: string, positionPrice: "left"/"center"/"right"} -->
  <a class="flex flex-col w-full  " :href="`https://dienthoaigiakho.vn/${productData.uri}`">
    <!-- {imgItemSrc} -->
    <figure class="relative w-full"><img class="w-full " :src="productData.image_source" alt="this is an image">
      <span
        :class="`absolute top-0 text-center w-full bg-[#ff0000] rounded-[5px] ${productData.flash_sale === true ? '' : 'hidden'}`">
        <p class="text-[13px]">FLASH SALE</p>
      </span>
    </figure>

    <!-- {itemPrice,positionPrice} -->
    <!-- tailwind text-{positionPrice} -->
    <span class="flex flex-wrap justify-between overflow-hidden">

      <span
        :class="`flex ${smallItems === 'true' ? 'flex-col text-[calc(15px*0.7)] ' : 'flex-row gap-[0.5rem] w-full text-[15px]'}`">
        <p :class="`line-through ${smallItems === 'true' ? 'text-[calc(15px*0.7)] w-full' : 'text-[18px] w-fit'}`">{{
          productData.price }} $</p>
        <p :class="`flex my-auto items-center ${smallItems === 'true' ? 'text-[calc(15px*0.7)]' : 'text-[18px]'}`">
          4.5
        <figure :class="`${smallItems === 'true' ? 'h-[calc(20px*0.5)] w-[calc(20px*0.5)]' : 'h-[18px] w-[18px]'}`">
          <svg class="w-full h-full" width="24" height="24" viewBox="0 0 48 48" fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <path
              d="M23.9986 5L17.8856 17.4776L4 19.4911L14.0589 29.3251L11.6544 43L23.9986 36.4192L36.3454 43L33.9586 29.3251L44 19.4911L30.1913 17.4776L23.9986 5Z"
              fill="#ffb100" stroke="#ffb100" stroke-width="4" stroke-linejoin="round" />
          </svg>
        </figure>
        </p>
      </span>

      <p
        :class="`my-auto text-right ${smallItems === 'true' ? 'w-[60%] text-[calc(22px*0.7)] ' : 'text-[24px] w-full'} `">
        {{
          productData.flash_price
        }}
        $</p>

      <span
        :class="`w-[100%] px-[3px] mt-[2%] text-center line-clamp-2 ${smallItems === 'true' ? 'text-[calc(15px*0.7)]' : 'text-[15px]'}`">
        {{
          productData.name }}</span>

    </span>
  </a>
</template>

<script>
export default {
  props: ['productData', 'positionPrice', 'smallItems'],
  setup() {
  }
}
</script>

<style scoped></style>