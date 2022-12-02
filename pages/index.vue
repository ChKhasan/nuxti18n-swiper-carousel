<template>
  <div class="homepage">
    <h1>{{ $t("welcometo") }}</h1>
    <a href="#">wewew</a>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  head: {
    css: ["~/assets/css/main"],
  },
  async asyncData({ $axios }) {
    const product = await $axios.$get("/products");

    console.log(product);
  },
};
</script>
<style lang="scss" scoped >
 @import "@/assets/css/main.css"; 
 .homepage h1 {
  &:hover {
    color: green;
  }
 }
</style>
