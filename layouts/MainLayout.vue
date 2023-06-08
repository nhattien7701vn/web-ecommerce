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

  <main id="main" class="mt-[100px] max-w-[1200px] items-center px-[2rem] my-0 mx-auto">
    <section id="hero-container" class="flex w-full h-[50vh] border-solid border-2 border-indigo-600">
      <div class="w-[25%] h-[100%] border-solid border-2 border-indigo-600">
        <h1 class="mt-[15rem]">Nav</h1>
      </div>
      <div class="flex flex-wrap w-[100%] h-[100%] border-solid border-2 border-indigo-600">
        <a class="basis-[100%] h-[2rem] w-[100%] bg-[#FFF5E6] " href="#">The a</a>
        <div class="basis-[70%] h-[100%] bg-[#000000]"></div>
        <div class="basis-[30%]"></div>
      </div>
    </section>
    <section id="content-container" class="flex-col w-full border-solid border-2 border-indigo-600">
      <section class="w-[100%] h-[10rem] border-solid border-2 border-indigo-600">
        <h1>flash sale section</h1>
      </section>
      <section class="flex flex-row w-[100%] h-[10rem] border-solid border-2 border-indigo-600">
        <section class="w-[50%] h-[100%] border-solid border-2 border-indigo-600">
          <h1>section 1</h1>
        </section>
        <section class="w-[50%] h-[100%] border-solid border-2 border-indigo-600">
          <h1>section 2</h1>
        </section>
      </section>
      <section class="flex flex-row w-[100%] h-[10rem] border-solid border-2 border-indigo-600">
        <h1>hot cate</h1>
      </section>
      <section class="flex flex-row w-[100%] h-[50vh] border-solid border-2 border-indigo-600">
        <h1>your choice cate</h1>
      </section>
    </section>
  </main>

  <section id="footer-container" class="w-[100%] h-[50vh] border-solid border-2 border-indigo-600">
    <h1>footer</h1>
  </section>

  <nav id="navbar-container" class="fixed z-50 top-[50%] right-0 translate-y-[-50%] w-[5rem] h-[10rem] bg-[#2d2d38]">
    navbar
  </nav>
</template>

<script setup>

</script>

