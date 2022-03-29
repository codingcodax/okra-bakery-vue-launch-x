<script setup>
import {
  IconChevronLeft,
  IconChevronRight,
} from "@/components/icons/index.vue";
import { ProductItem } from "@/components/atoms/index.vue";
import ProductsContainer from "@/components/containers/ProductsContainer.vue";
</script>

<template>
  <section class="customersFavorites">
    <h2 class="customersFavorites__title">Our Customer's Favorites</h2>
    <div class="customersFavorites__divider"></div>
    <ProductsContainer>
      <ProductItem
        src="/assets/img/christmas-cake.png"
        alt="christmas cake with forest fruits"
        isDelivery
        isAway
        isDining
      >
        <template #title>Christmas cake with forest fruits 500 g</template>
        <template #category>Chocolate noir &amp; fruits secs</template>
        <template #price>250</template>
      </ProductItem>
      <ProductItem
        src="/assets/img/royal-cake.png"
        alt="royal chocolate cake"
        isAway
        isDining
      >
        <template #title>Royal chocolate cake</template>
        <template #category>Chocolate noir &amp; fruits secs</template>
        <template #price>220</template>
      </ProductItem>
    </ProductsContainer>

    <div class="customersFavorites__buttons">
      <button class="customersFavorites__button"><IconChevronLeft /></button>
      <button class="customersFavorites__button"><IconChevronRight /></button>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.customersFavorites {
  margin-inline: auto;
  max-width: 1000px;

  &__title {
    font-size: 2rem;
    font-weight: normal;
    text-align: center;
    text-transform: uppercase;
  }

  &__divider {
    margin: 1rem auto 2rem;
    height: 2px;
    max-width: 50px;
    background-color: $gray12;
  }

  &__buttons {
    margin-inline: auto;
    width: fit-content;
    display: grid;
    grid-auto-flow: column;
    column-gap: 1rem;
  }

  &__button {
    padding: 0.5rem;
    margin-top: 2rem;
    color: $gray12;
    background-color: transparent;
    border: 1px solid $gray12;
    border-radius: 2rem;
    cursor: pointer;
    transition: 0.2s ease-in;
    transition-property: color, background-color;

    &:hover {
      color: $gray1;
      background-color: $gray12;
    }
  }
}
</style>
