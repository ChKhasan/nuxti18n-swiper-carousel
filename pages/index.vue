<template>
  <div class="homepage">
    <h1>{{ $t("welcometo") }}</h1>
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
<style lang="scss" scoped>
// @import "@/assets/css/main.css";
// @import "@/assets/css/swiper.css";
.homepage h1 {
  &:hover {
    color: green;
  }
}
</style>
