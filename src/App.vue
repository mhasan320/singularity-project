<template>
  <header>
    <HeaderComponent />
  </header>

  <RouterView />
</template>

<script setup>
import { RouterView } from "vue-router";
import HeaderComponent from "./components/HeaderComponent.vue";
</script>

<style lang="scss">
$color: red;
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
