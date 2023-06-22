<template>
  <section class="min-w-[19%] h-full border-solid border-2 border-indigo-600">
    <!-- <h1 class="" v-for="category in dataListCategory" :key="category.id">{{ category.name }}</h1> -->
    <ul class="flex flex-col w-full h-full ">
      <li class="py-[1rem] pl-[3rem]" v-for="category in dataListCategory" :key="category.id"><a
          :href="`https://dienthoaigiakho.vn/${category.uri}`">{{ category.name }}</a></li>
    </ul>
  </section>
</template>

<script>
export default {
  props: ['dataListCategory'],
  setup() {


    return {}
  }
}
</script>

<style lang="scss" scoped></style>