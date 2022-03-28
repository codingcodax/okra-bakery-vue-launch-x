<template>
  <ul class="products">
    <slot></slot>
  </ul>
</template>

<style lang="scss" scoped>
.products {
  padding: 0;
  display: grid;
  grid-template: auto / 1fr 1fr;
  gap: 2rem;
}
</style>
