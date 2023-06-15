<template>
  <h1>About page</h1>
  <button class="w-[50px] h-[50px] bg-[#000000]" onclick={}></button>
</template>

<script>
export default {
  testa() {
    console.log("hihihi");
  },
  async fetch() {
    console.log("hello im fetching API");
    const res = await fetch('http://localhost:3300/categories')
    const category = await res.json()
    console.log(category);
    return category
  }
}
</script>

