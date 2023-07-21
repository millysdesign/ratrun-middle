<template>
  <div>
    <AppHeader />

    <NuxtPage />

    <p>フッター</p>
  </div>
</template>

<script>
import { AppHeader } from "../components/organisms/Header";

export default {
  components: { AppHeader },
};
</script>

<style lang="scss" scoped>
p {
  padding-top: 50px;
}
</style>