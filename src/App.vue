<script setup>
import { RouterView } from "vue-router";
import { Header, FooterContainer } from "@/components/containers/index.vue";
</script>

<template>
  <Header />

  <div>
    <RouterView />
  </div>

  <FooterContainer />
</template>

<style lang="scss">
@use "@/assets/styles/base/reset";
@use "@/assets/styles/base/typography";
@use "@/assets/styles/base/global";
</style>
