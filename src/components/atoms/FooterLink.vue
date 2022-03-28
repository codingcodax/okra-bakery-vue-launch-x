<script setup>
defineProps({
  href: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <li class="link">
    <a :href="href" class="link__a">
      <slot></slot>
    </a>
  </li>
</template>

<style lang="scss" scoped>
.link {
  list-style-type: none;
  font-size: 0.9rem;

  &__a {
    text-decoration: none;
    transition: color 0.2s ease-in;

    &:hover {
      text-decoration: underline;
    }
  }
}
</style>
