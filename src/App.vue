<script>
import TheHeader from "./components/TheHeader.vue";
import CardList from "./components/CardList.vue";

export default {
  components: {
    TheHeader,
    CardList,
  },
};
</script>

<template>
  <TheHeader />
  <CardList />
</template>

<style lang="scss">
body {
  background-color: black;
}
</style>
