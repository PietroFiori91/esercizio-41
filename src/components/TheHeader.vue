<script>
import SearchBar from "./SearchBar.vue";
export default {
  components: { SearchBar },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="d-flex pt-4 gap-5">
        <img src="../assets/vue.svg" alt="" />
        <h3 class="">YO-API</h3>
      </div>
    </div>
  </header>
  <SearchBar />
</template>

<style scoped>
header {
  background-color: aliceblue;
  height: 100px;
}
</style>
