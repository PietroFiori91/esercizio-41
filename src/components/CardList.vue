<script>
import axios from "axios";
import { store } from "../store";

export default {
  data() {
    return {
      cards: [],
      store,
    };
  },
  methods: {
    fetchCards() {
      const url =
        "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0";

      axios.get(url).then((response) => {
        this.cards = response.data.data;
      });
    },
  },
  mounted() {
    this.fetchCards();
  },
};
</script>

<template>
  {{ store.searchText }}
  <div class="container">
    <div class="row row-cols-6">
      <div class="col my-5" v-for="card in cards" :key="cards.id">
        <div class="card h-100">
          <img
            :src="card.card_images[0].image_url"
            class="card-img-top"
            alt=""
          />
          <div class="card-body">
            <h5 class="card-title">{{ card.name }}</h5>
            <p class="card-text">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </p>
            <a href="#" class="btn btn-secondary">btn</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
