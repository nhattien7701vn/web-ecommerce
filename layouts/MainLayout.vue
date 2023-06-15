<template>
  <main id="main" class="mt-[100px] max-w-[100%] items-center  ">
    <section class="max-w-full bg-[#f7f7f7]">
      <section id="hero-container" class="flex gap-[0.5rem] w-[1200px] h-[56vh] my-0 mx-auto">
        <div class="w-[25%] h-[100%] border-solid border-2 border-indigo-600">
          <h1 class="mt-[15rem]">Nav</h1>
        </div>
        <div class="flex flex-col gap-[0.5rem] w-[100%] h-[100%]">
          <a class="w-[100%] h-[8%] bg-[#FFF5E6] " href="#">The a</a>
          <div class="flex flex-grow gap-[0.5rem] w-full">

            <div class="flex flex-col gap-[0.5rem] justify-between w-[65%]">

              <figure class="w-full h-[60%] overflow-hidden"><img class="w-full h-full rounded-[5px]"
                  src="/hero-promotion.jpg" alt="hinh anh"></figure>
              <div class="flex flex-grow gap-[0.7rem] flex-row w-full">
                <div class="h-[100%] grow bg-[#fff] rounded-[5px]">
                  COMPONENT 1
                </div>
                <div class="h-[100%] grow bg-[#fff] rounded-[5px]">
                  COMPONENT 2
                </div>
              </div>
            </div>

            <div class="flex flex-col gap-[0.7rem] flex-grow">
              <div class="w-full flex-grow border-solid border-2 border-indigo-600">promotion
              </div>
              <div class="w-full flex-grow border-solid border-2 border-indigo-600">promotion
              </div>
            </div>

          </div>
        </div>
      </section>
      <section id="content-container" class="flex-col w-[1200px] my-0 mx-auto">
        <section class="w-full p-[2%]">
          <!-- COMPONENT: itemChart -->
          <ItemChart chartTitle="Flash Deal" itemIconSeeInfo=false timeFlashSale=true dateLeft="" seeMoreBtn=true
            amountItem="6" dataListItem="" imgItemSrc="/item-img.png" itemPrice="100000" positionPrice="right" />
        </section>

        <section class="flex flex-row w-[100%] border-solid border-2 border-indigo-600">

          <section class="w-[50%] h-[100%] border-solid border-2 border-indigo-600">
            <!-- section 1 -->
            <section class="w-[100%] p-[1rem] border-solid border-2 border-indigo-600">
              <!-- COMPONENT: ItemChart -->
              <ItemChart />
            </section>
          </section>

          <section class="w-[50%] h-[100%] border-solid border-2 border-indigo-600">
            <!-- section 2 -->
            <section class="w-[100%] p-[1rem] border-solid border-2 border-indigo-600">
              <!-- COMPONENT: ItemChart -->
              <ItemChart />
            </section>
          </section>

        </section>

        <section class="flex flex-row w-[100%] h-[10rem] border-solid border-2 border-indigo-600">
          <h1>day ne</h1>
        </section>
      </section>
    </section>
    <section class="flex flex-row w-[100%] h-[50vh] border-solid border-2 border-indigo-600">
      <h1>your choice cate</h1>
    </section>

  </main>

  <section id="footer-container" class="w-[100%] h-[50vh] b order-solid border-2 border-indigo-600">
    <h1>footer</h1>

  </section>

  <nav id="navbar-container" class="fixed z-50 top-[50%] right-0 translate-y-[-50%] w-[2.3rem] h-[15rem] bg-[#2d2d38]">
    navbar
  </nav>
</template>

<script>
import ItemChart from '/components/ItemChart/ItemChart.vue';
// import postApi from '/api/postApi.mjs';
export default {
  components: {
    'ItemChart': ItemChart
  }

}
</script>
