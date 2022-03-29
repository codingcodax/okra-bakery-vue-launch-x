<script setup>
import { CategoryItem } from "@/components/atoms/index.vue";
</script>

<template>
  <ul class="categories">
    <CategoryItem
      src="/assets/img/new-years-treats.png"
      alt="cupcakes"
      href="#"
      >New Years Treats</CategoryItem
    >
    <CategoryItem src="/assets/img/special-cakes.png" alt="cakes" href="#"
      >Special Cakes</CategoryItem
    >
    <CategoryItem
      src="/assets/img/special-collection.png"
      alt="cupcakes"
      href="#"
      >Festival Collection</CategoryItem
    >
  </ul>
</template>

<style lang="scss" scoped>
.categories {
  padding: 0;
  margin: 2rem auto 4rem;
  max-width: 1000px;
  display: grid;
  grid-template: 1fr 1fr / 1fr 1fr;
  gap: 1.5rem;

  li:nth-child(1) {
    grid-row: 1 / -1;
  }
}
</style>
