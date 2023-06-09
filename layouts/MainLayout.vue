<template>
  <section id="header-container" class="fixed top-0 z-50 w-full py-[1rem] bg-[#2d2d38]">
    <header id="TopMenu" class="flex max-w-[1200px] items-center px-[2rem] my-0 mx-auto">
      <img class="w-[10rem] mr-[3.5rem]" src="/header-new-logo@2x.png" alt="">
      <div class="w-[45%]">
        <div class="w-[100%] relative">
          <input class="w-[100%] h-[2.5rem] rounded-[5px]" type="text">
          <button
            class="absolute top-[50%] right-0 translate-x-[0] translate-y-[-50%] px-[0.5rem] h-full bg-[#FF6E26] rounded-[5px]">
            <svg width="24" height="24" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M21 38C30.3888 38 38 30.3888 38 21C38 11.6112 30.3888 4 21 4C11.6112 4 4 11.6112 4 21C4 30.3888 11.6112 38 21 38Z"
                fill="#ffffff" stroke="#ffffff" stroke-width="4" stroke-linejoin="round" />
              <path d="M26.657 14.3431C25.2093 12.8954 23.2093 12 21.0001 12C18.791 12 16.791 12.8954 15.3433 14.3431"
                stroke="#FFF" stroke-width="4" stroke-linecap="round" stroke-linejoin="round" />
              <path d="M33.2216 33.2217L41.7069 41.707" stroke="#ffffff" stroke-width="4" stroke-linecap="round"
                stroke-linejoin="round" />
            </svg>
          </button>
        </div>
        <ul class="flex text-[0.8rem] gap-[1rem]">
          <li><a href="">dien thoai</a></li>
          <li><a href="">man hinh</a></li>
          <li><a href="">ban phim </a></li>
          <li><a href="">quan ao</a></li>
          <li><a href="">may tinh bang</a></li>
          <li><a href="">binh nuoc</a></li>
          <li><a href="">quat may</a></li>
        </ul>
      </div>
    </header>
  </section>

  <main id="main" class="mt-[100px] max-w-[100%] items-center  ">
    <section class="max-w-full bg-[#f7f7f7]">
      <section id="hero-container" class="flex w-[1200px] h-[56vh] my-0 mx-auto">
        <div class="w-[25%] h-[100%] border-solid border-2 border-indigo-600">
          <h1 class="mt-[15rem]">Nav</h1>
        </div>
        <div class="flex flex-wrap gap-[0.5rem] w-[100%] h-[100%]">
          <a class="basis-[100%] w-[100%] h-[2rem] bg-[#FFF5E6] " href="#">The a</a>
          <div class="flex flex-row flex-wrap gap-[0.7rem] w-[64%] h-[calc(100%-2rem-0.7rem)]">
            <figure class="basis-[100%] h-[62%] overflow-hidden"><img class="w-full h-full rounded-[5px]"
                src="/hero-promotion.jpg" alt="hinh anh"></figure>
            <div class="w-[49%] h-[33%] grow bg-[#fff] rounded-[5px]">COMPONENT 1</div>
            <div class="w-[49%] h-[33%] grow bg-[#fff] rounded-[5px]">COMPONENT 2</div>
          </div>
          <div class="flex-grow">
            <div class="w-full h-[50%] border-solid border-2 border-indigo-600">promotion
            </div>
            <div class="w-full h-[50%] border-solid border-2 border-indigo-600">promotion
            </div>
          </div>
        </div>
      </section>
      <section id="content-container" class="flex-col w-[1200px] my-0 mx-auto">
        <section class="w-[100% p-[1rem] border-solid border-2 border-indigo-600">
          <!-- COMPONENT: itemChart -->
          <section class="flex flex-col w-full h-full">
            <!-- top-container -->
            <div class="flex w-full items-center justify-between">
              <!-- top-container left -->
              <div class="flex items-center gap-[0.5rem]">
                <!-- REQUIRED: chartTitle: sting -->
                <a href="#" class="font-bold text-[1.5rem]">{chartTitle}</a>
                <!-- REQUIRED: itemIconSeeInfo: "<svg>...</svg>" -->
                <!-- {itemIconSeeInfo} -->
                <a href="#">
                  <svg width="24" height="24" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                      d="M24 44C35.0457 44 44 35.0457 44 24C44 12.9543 35.0457 4 24 4C12.9543 4 4 12.9543 4 24C4 35.0457 12.9543 44 24 44Z"
                      fill="none" stroke="#000000" stroke-width="4" stroke-linejoin="round" />
                    <path d="M21 33L30 24L21 15" stroke="#000000" stroke-width="4" stroke-linecap="round"
                      stroke-linejoin="round" />
                  </svg>
                </a>
                <!-- REQUIRED: chartFlashSale: boolean-->
                <!-- if true show flash sale  -->
                <!-- else hide flash sale -->
                <!-- count down timer  -->
                <ul class="flex h-[24px] gap-[4px] text-[#ffffff]">
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
              <a href="#" class="text-[0.9rem]">Xem thêm</a>
            </div>

            <!-- list items -->
            <!-- REQUIRED: {amountItem: number, dataListItem: array} -->
            <ul class="flex flex-row flex-wrap gap-[0.8rem]">
              <!-- map this array to each item -->
              <!-- this <li> has flex-basis=calc(100%/{amountItem}-gap*{amountItem}) -->
              <!-- map this array to each item -->
              <li class="flex basis-[calc(100%/6-0.7rem)]">
                <!-- component items  -->
                <!-- REQUIRED: {imgItemSrc: string, itemPrice: string, positionPrice: "left"/"center"/"right"} -->
                <a class="flex flex-col w-full h-full" href="#">
                  <!-- {imgItemSrc} -->
                  <img class="w-full" src="/item-img.png" alt="this is an image">
                  <!-- {itemPrice,positionPrice} -->
                  <!-- tailwind text-{positionPrice} -->
                  <p class="w-full text-left">{itemPrice}</p>
                </a>
              </li>

            </ul>
          </section>
        </section>

        <section class="flex flex-row w-[100%] border-solid border-2 border-indigo-600">
          
          <section class="w-[50%] h-[100%] border-solid border-2 border-indigo-600">

            <!-- section 1 -->
            <section class="w-[100% p-[1rem] border-solid border-2 border-indigo-600">
              <!-- COMPONENT: itemChart -->
              <section class="flex flex-col w-full h-full">
                <!-- top-container -->
                <div class="flex w-full items-center justify-between">
                  <!-- top-container left -->
                  <div class="flex items-center gap-[0.5rem]">
                    <!-- REQUIRED: chartTitle: sting -->
                    <a href="#" class="font-bold text-[1.5rem]">{chartTitle}</a>
                    <!-- REQUIRED: itemIconSeeInfo: "<svg>...</svg>" -->
                    <!-- {itemIconSeeInfo} -->
                    <a href="#">
                      <svg width="24" height="24" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M24 44C35.0457 44 44 35.0457 44 24C44 12.9543 35.0457 4 24 4C12.9543 4 4 12.9543 4 24C4 35.0457 12.9543 44 24 44Z"
                          fill="none" stroke="#000000" stroke-width="4" stroke-linejoin="round" />
                        <path d="M21 33L30 24L21 15" stroke="#000000" stroke-width="4" stroke-linecap="round"
                          stroke-linejoin="round" />
                      </svg>
                    </a>
                    <!-- REQUIRED: chartFlashSale: boolean-->
                    <!-- if true show flash sale  -->
                    <!-- else hide flash sale -->
                    <!-- count down timer  -->
                    <ul class="flex h-[24px] gap-[4px] text-[#ffffff]">
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
                  <a href="#" class="text-[0.9rem]">Xem thêm</a>
                </div>

                <!-- list items -->
                <!-- REQUIRED: {amountItem: number, dataListItem: array} -->
                <ul class="flex flex-row flex-wrap gap-[0.8rem]">
                  <!-- map this array to each item -->
                  <!-- this <li> has flex-basis=calc(100%/{amountItem}-gap*{amountItem}) -->
                  <!-- map this array to each item -->
                  <li class="flex basis-[calc(100%/6-0.7rem)]">
                    <!-- component items  -->
                    <!-- REQUIRED: {imgItemSrc: string, itemPrice: string, positionPrice: "left"/"center"/"right"} -->
                    <a class="flex flex-col w-full h-full" href="#">
                      <!-- {imgItemSrc} -->
                      <img class="w-full" src="/item-img.png" alt="this is an image">
                      <!-- {itemPrice,positionPrice} -->
                      <!-- tailwind text-{positionPrice} -->
                      <p class="w-full text-left">{itemPrice}</p>
                    </a>
                  </li>

                </ul>
              </section>
            </section>
            <!-- section 1 -->

          </section>
          <section class="w-[50%] h-[100%] border-solid border-2 border-indigo-600">
            


          </section>
        </section>

        <section class="flex flex-row w-[100%] h-[10rem] border-solid border-2 border-indigo-600">
          <h1>hot cate</h1>
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

<script setup>

</script>

