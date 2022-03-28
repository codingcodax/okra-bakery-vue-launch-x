<script setup>
import { NavLink } from "@/components/atoms/index.vue";
</script>

<template>
  <nav class="nav">
    <ul class="nav__links">
      <NavLink href="#">Cakes</NavLink>
      <NavLink href="#">Pastries</NavLink>
      <NavLink href="#">Bakery</NavLink>
      <NavLink href="#">Seasonal</NavLink>
      <NavLink href="#">Buffer</NavLink>
      <NavLink href="#">Workshop</NavLink>
      <NavLink href="#">Contact</NavLink>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.nav {
  border-top: 1px solid lightgray;

  &__links {
    padding: 0.5rem 0;
    margin-inline: auto;
    width: 100%;
    max-width: 1000px;
    display: grid;
    grid-auto-flow: column;
  }
}
</style>
