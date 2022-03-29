<script setup>
import { RouterLink } from "vue-router";

import { IconSearch, IconAccount, IconBag } from "@/components/icons/index.vue";
import Logo from "@/components/atoms/LogoComponent.vue";
import { NavLinks } from "./links/index.vue";
</script>

<template>
  <header class="header">
    <div class="header__container">
      <Logo />

      <ul class="header__links">
        <li>
          <IconSearch />
        </li>
        <li class="header__link">
          <RouterLink to="/account"><IconAccount /></RouterLink>
        </li>
        <li class="header__link">
          <RouterLink to="/cart"><IconBag /></RouterLink>
        </li>
      </ul>
    </div>

    <NavLinks />
  </header>
</template>

<style lang="scss" scoped>
.header {
  &__container {
    padding: 1rem 0;
    margin-inline: auto;
    width: 100%;
    max-width: 1000px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__links {
    padding: 0;
    list-style-type: none;
    display: grid;
    grid-auto-flow: column;
    grid-column-gap: 1rem;
    align-items: center;
  }

  &__link {
    height: 2rem;
    width: 2rem;
    display: grid;
    place-items: center;
  }
}
</style>
