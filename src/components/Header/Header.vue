<template>
  <div id="MainLayout" class="w-full fixed z-50">
    <div id="TopMenu" class="w-full bg-[#FAFAFA] border-b md:black hidden"></div>
    <ul class="
                        flex
                        items-center
                        justify-end
                        text-xs
                        text-[#333333]
                        font-light
                        px-2
                        h-10
                        bg-[#FAFAFA]
                        max-w-[1200px]">
      <li class="border-r border-r-gray-400 px-3 hover:text-[#FF4646] cursor-pointer">
        Sell on Aliexpress
      </li>
      <li class="border-r border-r-gray-400 px-3 hover:text-[#FF4646] cursor-pointer">
        Cookie Preferences
      </li>
      <li class="border-r border-r-gray-400 px-3 hover:text-[#FF4646] cursor-pointer">
        Help
      </li>
      <li class="border-r border-r-gray-400 px-3 hover:text-[#FF4646] cursor-pointer">
        Buyer Protection
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>
<style scoped>
/* CSS styles chỉ áp dụng cho Header component */
header {
  background-color: #f0f0f0;
  padding: 20px;
  /* Các styles khác */
}

h1 {
  color: #333;
  font-size: 24px;
  /* Các styles khác */
}
</style>
