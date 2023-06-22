<template>
  <!-- component items  -->
  <!-- REQUIRED: {imgItemSrc: string, itemPrice: string, positionPrice: "left"/"center"/"right"} -->
  <a class="flex flex-col w-full h-full" :href="`https://dienthoaigiakho.vn/${productData.uri}`">
    <!-- {imgItemSrc} -->
    <figure class="w-full"><img class="w-full " :src="productData.image_source" alt="this is an image"></figure>
    <!-- {itemPrice,positionPrice} -->
    <!-- tailwind text-{positionPrice} -->
    <p :style="{ textAlign: positionPrice }" class="text-[16px]	"
      :class="`${titleSize === 'small' ? '' : 'line-through'}`">{{ productData.price }} $</p>
    <p :style="{ textAlign: positionPrice }" :class="`text-[18px] ${titleSize === 'small' ? 'hidden' : 'block'}`">{{
      productData.flash_price }} $</p>
    <!-- <p class=" line-through	text-[13px]">{{ productData.price }} $</p>
      <p class=" line-through	text-[13px]">{{ productData.price }} $</p> -->
  </a>
</template>

<script>
export default {
  props: ['productData', 'positionPrice', 'titleSize'],
  setup() {
  }
}
</script>

<style scoped></style>