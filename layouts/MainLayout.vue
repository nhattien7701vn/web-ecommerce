<template>
  <main id="main" class="mt-[100px] max-w-[100%] items-center  ">
    <section class="max-w-full bg-[#f7f7f7]">
      <section id="hero-container" class="flex gap-[0.5rem] w-[1200px] h-[56vh] my-0 mx-auto">
        <NavMenu :dataListCategory="categories" />
        <div class="flex flex-col gap-[0.5rem] w-[100%] h-[100%]">

          <a class="w-[100%] h-[8%] pl-[1rem] bg-[#FFF5E6] text-[15px] " href="#">(CN)Giao hàng ưu tiên Banggood miễn phí cho các đơn hàng trên 1.192.376₫</a>

          <div class="flex flex-grow gap-[0.5rem] w-full">

            <!-- HERO & FLASH DEAL -->
            <div class="flex flex-col gap-[0.5rem] justify-between max-w-[65%]">

              <figure class="w-full h-[60%] overflow-hidden"><img class="w-full h-full rounded-[5px]"
                  src="/hero-promotion.jpg" alt="hinh anh"></figure>
              <div class="flex flex-grow gap-[0.7rem] flex-row w-full">
                <div class="h-[100%] w-[50%] p-[0.5rem]">
                  <ItemChart chartTitle="Flash Deal" itemIconSeeInfo=false timeFlashSale=false seeMoreBtn=false
                    :dataListProduct="products" positionPrice="center" amountItemDisplay="3" displayInline=true titleSize="small"/>
                </div>

                <div class="h-[100%] w-[50%] p-[0.5rem]">
                  <ItemChart chartTitle="Flash Deal" itemIconSeeInfo=false timeFlashSale=false seeMoreBtn=false
                    :dataListProduct="products" positionPrice="center" amountItemDisplay="3" displayInline=true titleSize="small" />
                </div>
              </div>
            </div>
            <!-- PROMOTION -->
            <div class="flex flex-col gap-[0.7rem] flex-grow">
              <div class="w-full flex-grow border-solid border-2 border-indigo-600">promotion
              </div>
              <div class="w-full flex-grow border-solid border-2 border-indigo-600">promotion
              </div>
            </div>

          </div>

        </div>
      </section>

      <!-- CONTENT -->
      <section id="content-container" class="flex-col w-[1200px] my-0 mx-auto">
        <section class="w-full p-[2%]">
          <!-- COMPONENT: itemChart -->
          <ItemChart chartTitle="Flash Deal" itemIconSeeInfo=false timeFlashSale=true dateLeft="" seeMoreBtn=true
            :dataListProduct="products" positionPrice="left" amountItemDisplay="6" displayInline=true />
        </section>

        <section class="flex flex-row flex-wrap w-[100%] ">
          <section class="w-[50%] h-full p-[1rem]">
            <ItemChart chartTitle="HOT DEAL 1" itemIconSeeInfo=false timeFlashSale=false dateLeft="" seeMoreBtn=false
              :dataListProduct="products" positionPrice="left" amountItemDisplay="3" displayInline=true />
          </section>
          <section class="w-[50%] h-full p-[1rem]">
            <ItemChart chartTitle="HOT DEAL 2" itemIconSeeInfo=false timeFlashSale=false dateLeft="" seeMoreBtn=false
              :dataListProduct="products" positionPrice="left" amountItemDisplay="3" displayInline=true />
          </section>
        </section>

        <section class="flex flex-row w-[100%] p-[1rem]">
          <ItemChart chartTitle="MENU" itemIconSeeInfo=false timeFlashSale=false dateLeft="" seeMoreBtn=true
            :dataListProduct="products" positionPrice="left" amountItemDisplay="6" />
        </section>
      </section>

    </section>

    <!-- YOUR CHOICE -->
    <section class="flex flex-row w-[100%] h-[50vh] border-solid border-2 border-indigo-600">
      <h1>your choice cate</h1>
    </section>

  </main>

  <!-- FOOTER -->
  <section id="footer-container" class="w-[100%] h-[50vh] b order-solid border-2 border-indigo-600">
    <h1>footer</h1>

  </section>

  <!-- NAV BAR -->
  <nav id="navbar-container" class="fixed z-50 top-[50%] right-0 translate-y-[-50%] w-[2.3rem] h-[15rem] bg-[#2d2d38]">
    navbar
  </nav>
</template>

<script setup>
definePageMeta({
  layout: "products"
})
import ItemChart from '/components/ItemChart/ItemChart.vue';
// import { ref } from "vue";
// const productData = ref()
const { data: products } = await useFetch('https://web-ecommerce-api.vercel.app/products')
const { data: categories } = await useFetch('https://web-ecommerce-api.vercel.app/categories')
</script>
