<template>
  <div class="logo">
    <h2 class="logo__title">Okra</h2>
    <h3 class="logo__subtitle">Sweet Bakery</h3>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/abstracts/variables" as *;

.logo {
  color: $primary9;

  &__title {
    font-size: 1.5rem;
    text-transform: uppercase;
  }

  &__subtitle {
    font-size: 0.8rem;
    font-weight: normal;
    text-transform: uppercase;
  }
}
</style>
