<template lang="html">
  <div>
    <nuxt-link :to="localePath('/')">Home</nuxt-link>
    <nuxt-link :to="localePath('/about')">about</nuxt-link>
    <nuxt-link :to="localePath('/swipers')">swipers</nuxt-link>
    <nuxt-link :to="switchLocalePath('fr')">Français</nuxt-link>
    <nuxt-link :to="switchLocalePath('es')">es</nuxt-link>
    <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
    <button @click="lang('en')">en</button>
    <button @click="lang('fr')">fr</button>
    <button @click="lang('es')">es</button>
    <Nuxt />
  </div>
</template>
<script>
export default {
  methods: {
    lang(val) {
      this.$i18n.setLocale(val);
    },
  },
};
</script>
<style lang="css"></style>
