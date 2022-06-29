<template>
  <div id="app">
    <search-bar />
    <product-list />
  </div>
</template>

<script>
import SearchBar from "./components/SearchBar.vue";
import ProductList from "./components/ProductList.vue";
export default {
  name: "App",
  components: { SearchBar, ProductList },
};
</script>

<style lang="scss">
</style>
