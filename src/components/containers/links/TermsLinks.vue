<script setup>
import { FooterLink } from "@/components/atoms/index.vue";
</script>

<template>
  <ul class="links">
    <p class="links__title">Our Terms &amp; Conditions</p>
    <FooterLink href="#">Our terms of delivery</FooterLink>
    <FooterLink href="#">Terms of sale</FooterLink>
    <FooterLink href="#">Cookies</FooterLink>
    <FooterLink href="#">Privacy Policy</FooterLink>
    <FooterLink href="#">Delivery Policy</FooterLink>
    <FooterLink href="#">FAQ</FooterLink>
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
