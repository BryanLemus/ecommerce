<template>
  <navbar placeholder="¿Qué puedo encontrar para ti?" />
  <router-view />
</template>

<script>
import navbar from "./components/Navbar";
export default {
  components: {
    navbar,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/styles";
</style>
