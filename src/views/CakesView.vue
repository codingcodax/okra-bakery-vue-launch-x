<script setup>
import {
  ProductHeaderSection,
  AllProductsSection,
} from "@/components/containers/sections/index.vue";
</script>

<template>
  <ProductHeaderSection
    src="/img/assortment-pieces-cake.png"
    alt="assortment cake in pieces"
  >
    <template #title>Cakes</template>
    <template #description
      >From Chocolate Cakes, to Fruity Cakes, to cheesecakes and so many more,
      there is a cake for any celebration and occasion. Why not personalize a
      special birthday message on your chosen cake to make the celebration extra
      special.</template
    >
  </ProductHeaderSection>
  <AllProductsSection />
</template>
