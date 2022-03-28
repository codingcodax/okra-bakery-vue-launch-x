<script setup>
defineProps({
  src: {
    type: String,
    required: true,
  },
  alt: {
    type: String,
    required: true,
  },
  href: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <li class="category">
    <img :src="src" :alt="alt" class="category__image" />
    <h3 class="category__title"><slot></slot></h3>
    <a :href="href" class="category__link">Shop Now</a>
  </li>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.category {
  list-style-type: none;
  display: grid;
  grid-template-rows: 1fr auto auto;

  &__image {
    height: 100%;
    width: 100%;
    object-fit: cover;
  }

  &__title {
    font-size: 1rem;
    font-weight: normal;
    text-transform: uppercase;
  }

  &__link {
    width: max-content;
    font-size: 0.8rem;
    text-transform: capitalize;
    text-decoration: none;
    border-bottom: 1px solid $primary9;
  }
}
</style>
