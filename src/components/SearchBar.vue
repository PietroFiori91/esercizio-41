<script>
import { store } from "../store";
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container my-4">
    <div class="input-group mb-3">
      <input
        type="text"
        class="form-control"
        placeholder="Search..."
        aria-label="Recipient's username"
        aria-describedby="button-addon2"
        v-model="store.searchText"
      />
      <button
        class="btn btn-outline-secondary"
        type="button"
        id="button-addon2"
      >
        Go !
      </button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.container {
  width: 30%;
}
</style>
