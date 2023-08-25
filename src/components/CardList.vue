<script>
import axios from "axios";

export default {
  data() {
    return {
      cards: [],
    };
  },
  methods: {
    fetchCards() {
      const url =
        "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0";

      axios.get(url).then((response) => {
        this.cards = response.data.results;
      });
    },
  },
  mounted() {
    this.fetchCards();
  },
};
</script>

<template></template>

<style lang="scss" scoped></style>
