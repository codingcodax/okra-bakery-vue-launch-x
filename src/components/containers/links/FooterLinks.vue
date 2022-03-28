<script setup>
import { CollectionsLinks, TermsLinks } from "./index.vue";
</script>

<template>
  <div class="footerLinks">
    <CollectionsLinks />
    <TermsLinks />
  </div>
</template>

<style lang="scss" scoped>
.footerLinks {
  display: grid;
  grid-auto-flow: column;
  column-gap: 1rem;
}
</style>
