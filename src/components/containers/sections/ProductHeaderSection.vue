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
})
</script>

<template>
  <div class="productHeader">
    <img class="productHeader__image" :src="src" :alt="alt" />
    <section class="productHeader__content">
      <h1 class="productHeader__title"><slot name="title"></slot></h1>
      <div class="productHeader__divider"></div>
      <p class="productHeader__description"><slot name="description"></slot></p>
      <button class="productHeader__button">Load More</button>
    </section>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;
@use "@/assets/styles/abstracts/mixins" as *;

.productHeader {
  margin-bottom: 6rem;
  position: relative;
  display: grid;
  grid-template-rows: repeat(5, 1fr);

  &__image {
    grid-row: 1 / span 3;
    height: 100%;
    width: 100%;
    position: absolute;
    object-fit: cover;
    filter: brightness(40%);
  }

  &__content {
    grid-row: 3 / -1;
    padding: 2rem;
    margin-inline: auto;
    width: 100%;
    max-width: 1000px;
    background-color: $primary2;
    z-index: 2;
  }

  &__title {
    font-size: 2rem;
    font-weight: normal;
    text-align: center;
    text-transform: uppercase;
  }

  &__divider {
    margin: 0.25rem auto 2rem;
    height: 2px;
    max-width: 80px;
    background-color: $gray12;
  }

  &__description {
    margin-inline: auto;
    max-width: 80ch;
    text-align: center;
  }

  &__button {
    @include secondaryButton();

    display: block;
    margin: 1rem auto 0;
  }
}
</style>
