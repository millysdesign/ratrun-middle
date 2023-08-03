<template>
  <div>
    <AppHeader class="app-header" />

    <NuxtPage />

    <AppFooter />
  </div>
</template>

<script>
import { AppHeader } from "../components/organisms/Header";
import { AppFooter } from "../components/organisms/Footer";
export default {
  components: { AppHeader, AppFooter },
};
</script>

<style lang="scss" scoped>
.app-header {
  padding-bottom: 50px;
}
</style>