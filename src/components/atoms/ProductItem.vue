<script setup>
import {
  IconTruckFast,
  IconBagItemInside,
  IconChairs,
  IconShoppingCart,
} from "@/components/icons/index.vue";

defineProps({
  src: {
    type: String,
    required: true,
  },
  alt: {
    type: String,
    required: true,
  },
  isDelivery: Boolean,
  isAway: Boolean,
  isDining: Boolean,
});
</script>

<template>
  <li class="product">
    <img class="product__image" :src="src" :alt="alt" />
    <div class="product__data">
      <h3 class="product__title"><slot name="title"></slot></h3>
      <p class="product__category"><slot name="category"></slot></p>
      <span class="product__price">$ <slot name="price"></slot></span>
      <div class="product__divider"></div>
      <span :class="`product__feature ${isDelivery}`"><IconTruckFast /> Home Delivery</span>
      <span :class="`product__feature ${isAway}`"
        ><IconBagItemInside /> Take Away</span
      >
      <span :class="`product__feature ${isDining}`"><IconChairs /> Dining</span>
      <button class="product__link"><IconShoppingCart /> Add to cart</button>
    </div>
  </li>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;
@use "@/assets/styles/abstracts/mixins" as *;

.product {
  list-style-type: none;
  display: grid;
  grid-template: auto / 1fr 1fr;
  border: 1px solid $gray6;

  &__data {
    padding: 1rem 1rem 1rem 0;
    display: flex;
    flex-direction: column;
  }

  &__title {
    font-size: 1rem;
    text-transform: uppercase;
  }

  &__category {
    color: $gray11;
    font-size: 0.9rem;
  }

  &__price {
    margin-top: 1rem;
    font-size: 1.2rem;
    font-weight: bold;
  }

  &__divider {
    margin: 0.5rem 0;
    height: 1px;
    background-color: $gray6;
  }

  &__feature {
    color: $gray11;
    font-size: 0.9rem;
    text-transform: capitalize;
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 0.5rem;
    align-items: center;

    &.true {
      color: $green9;
    }
  }

  &__link {
    @include primaryButton;

    margin-top: 1rem;
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 0.5rem;
    align-items: center;
  }
}
</style>
