<script setup>
import { FooterLink } from "@/components/atoms/index.vue";
</script>

<template>
  <ul class="links">
    <p class="links__title">Collections</p>
    <FooterLink href="#">Home</FooterLink>
    <FooterLink href="#">Cakes</FooterLink>
    <FooterLink href="#">Order Online</FooterLink>
    <FooterLink href="#">Occasions</FooterLink>
    <FooterLink href="#">About</FooterLink>
    <FooterLink href="#">Media</FooterLink>
    <FooterLink href="#">Contact</FooterLink>
  </ul>
</template>

<style lang="scss" scoped>
.links {
  padding: 0;
  display: grid;
  row-gap: 0.3rem;

  &__title {
    margin-bottom: 0.5rem;
    text-transform: uppercase;
  }
}
</style>
