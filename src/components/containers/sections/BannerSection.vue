<script setup>
import { IconChevronRight } from "@/components/icons/index.vue";
</script>


<template>
  <section class="banner">
    <img
      class="banner__image"
      src="@/assets/img/waffle-cakes.png"
      alt="yummy waffle cakes with fresh fruits"
    />

    <div class="banner__content">
      <div>
        <h1 class="banner__title">Happy new year</h1>
        <p class="banner__subtitle">Discover our festive range</p>
        <a href="#" class="banner__link">Shop Now <IconChevronRight /></a>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.banner {
  position: relative;
  color: $gray1;
  display: flex;
  align-items: center;

  &__image {
    width: 100%;
    filter: brightness(40%);
  }

  &__content {
    width: 100%;
    position: absolute;
    z-index: 1;

    & div {
      margin-inline: auto;
      width: 100%;
      max-width: 1000px;
    }
  }

  &__title {
    font-size: 3rem;
  }

  &__subtitle {
    font-size: 1.5rem;
  }

  &__link {
    color: $gray12;
    background-color: $gray1;
    display: flex;
    align-items: center;

    margin-top: 1rem;
    width: max-content;
    padding: 0.8rem 1.2rem;
    // display: inline-block;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2rem;
    transition: background-color, color 0.2s ease-in;

    &:hover {
      color: $gray1;
      background-color: $primary9;

      & svg {
        color: primary9;
      }
    }

    & svg {
      margin-left: 0.5rem;
    }
  }
}
</style>
