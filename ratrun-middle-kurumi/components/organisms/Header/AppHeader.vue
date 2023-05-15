<template>
  <!-- html -->
  <div class="header">
    <nav class="nav">
      <ul class="nav-list">
        <li v-for="(page, key) in pageList" :key="key">
          <nuxt-link to="#">{{ page.title }}</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
// js
export default {
  setup() {
    const pageList = ref([
      { title: "ホーム" },
      { title: "経営理念" },
      { title: "事業理念" },
      { title: "事業目的" },
      { title: "お問い合わせ" },
    ]);
    return { pageList };
  },
};
</script>

<style lang='scss' scoped>
// CSS
.nav {
  .nav-list {
    list-style: none;
    display: flex;
    color: black;
    li {
      margin-right: 20px;
    }
  }
}
</style>
