<script setup>
import { IconChevronDown } from "@/components/icons/index.vue";

defineProps({
  href: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <li class="navLink">
    <a :href="href" class="navLink__a">
      <slot></slot>
      <IconChevronDown />
    </a>
  </li>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.navLink {
  list-style-type: none;
  text-align: center;
  justify-self: center;

  &__a {
    width: max-content;
    text-decoration: none;
    display: flex;
    align-items: center;

    transition: color 0.2s ease-in;

    &:hover {
      color: $primary9;

      & svg {
        color: $primary9;
      }
    }

    & svg {
      margin-left: 0.5rem;
      transition: 0.2s ease-in;
    }
  }
}
</style>
