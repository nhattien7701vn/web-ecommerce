<template>
  <!-- component items  -->
  <!-- REQUIRED: {imgItemSrc: string, itemPrice: string, positionPrice: "left"/"center"/"right"} -->
  <a class="flex flex-col w-full h-full" href="#">
    <!-- {imgItemSrc} -->
    <img class="w-full h-full" :src="imgItemSrc" alt="this is an image">
    <!-- {itemPrice,positionPrice} -->
    <!-- tailwind text-{positionPrice} -->
    <p :style="{ textAlign: positionPrice }" class="w-full">{{ itemPrice }}</p>
  </a>
</template>

<script>
export default {
  props: ['imgItemSrc', 'itemPrice', 'positionPrice']
}
</script>

<style scoped></style>