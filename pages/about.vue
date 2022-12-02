<template lang="html">
  <div>
    <h1>{{ $t("welcometo") }}</h1>
    <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
    <nuxt-link :to="switchLocalePath('fr')">Français</nuxt-link>
    <nuxt-link to="/">Home</nuxt-link>
    <nuxt-link to="/about">about</nuxt-link>
  </div>
</template>
<script>

