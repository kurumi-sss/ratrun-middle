<template>
  <div>
    <AppHeader />
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

<style lang='scss' scoped>
</style>
