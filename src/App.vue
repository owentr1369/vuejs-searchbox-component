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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Varela Round", sans-serif;
}
#app {
  width: 100%;
  min-height: 100vh;
  display: flex;
  align-items: center;
  flex-direction: column;
}
</style>
