<script setup>
import { ProductItem } from "@/components/atoms/index.vue";
import ProductsContainer from "@/components/containers/ProductsContainer.vue";

const products = [
  {
    title: "Christmas cake with forest fruits 500 g",
    category: "Chocolat noir & fruits secs",
    price: "70",
    src: "/src/assets/img/christmas-cake.png",
    alt: "christmas cake with forest fruits",
    isDelivery: true,
    isAway: true,
    isDining: true,
  },
  {
    title: "Royal chocolate cake",
    category: "Chocolat noir & fruits secs",
    price: "62",
    src: "/src/assets/img/royal-cake.png",
    alt: "royal chocolate cake",
    isDelivery: false,
    isAway: true,
    isDining: true,
  },
  {
    title: "Mango coconut entremets cake",
    category: "Chocolat noir & fruits secs",
    price: "45",
    src: "/src/assets/img/mango-coconut-entremets-cake.png",
    alt: "mango coconut entremets cake",
    isDelivery: true,
    isAway: true,
    isDining: false,
  },
  {
    title: "Vanilla pancake sprinkled",
    category: "Chocolat noir & fruits secs",
    price: "10",
    src: "/src/assets/img/pancake-yellow.png",
    alt: "vanilla pancake with red sprinkled",
    isDelivery: false,
    isAway: false,
    isDining: true,
  },
  {
    title: "Rainbow pinata cake",
    category: "Chocolat noir & fruits secs",
    price: "65",
    src: "/src/assets/img/rainbow-pinata-cake-sliced.png",
    alt: "rainbow pinata cake sliced",
    isDelivery: true,
    isAway: true,
    isDining: true,
  },
  {
    title: "Lemon raspberry ripple cake",
    category: "Chocolat noir & fruits secs",
    price: "69",
    src: "/src/assets/img/lemon-raspberry-ripple-cake.png",
    alt: "lemon raspberry ripple cake",
    isDelivery: true,
    isAway: false,
    isDining: true,
  },
];
</script>

<template>
  <section class="products">
    <ProductsContainer>
      <ProductItem
        v-for="product in products"
        :key="product.title"
        :src="product.src"
        :alt="product.alt"
        :isDelivery="product.isDelivery"
        :isAway="product.isAway"
        :isDining="product.isDining"
      >
        <template #title>{{ product.title }}</template>
        <template #category>{{ product.category }}</template>
        <template #price>{{ product.price }}</template>
      </ProductItem>
    </ProductsContainer>
  </section>
</template>

<style lang="scss" scoped>
.products {
  margin-inline: auto;
  max-width: 1000px;
}
</style>
