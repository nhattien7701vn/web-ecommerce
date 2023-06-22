<template>
  <!-- component items  -->
  <!-- REQUIRED: {imgItemSrc: string, itemPrice: string, positionPrice: "left"/"center"/"right"} -->
  <a class="flex flex-col w-full " :href="`https://dienthoaigiakho.vn/${productData.uri}`">
    <!-- {imgItemSrc} -->
    <figure class="w-full h-full"><img class="w-full " :src="productData.image_source" alt="this is an image"></figure>
    <!-- {itemPrice,positionPrice} -->
    <!-- tailwind text-{positionPrice} -->
    <p :style="{ textAlign: positionPrice }" class="w-full">{{ productData.price }} $</p>
  </a>
</template>

<script>
export default {
  props: ['productData', 'positionPrice'],
  setup() {
  }
}
</script>

<style scoped></style>