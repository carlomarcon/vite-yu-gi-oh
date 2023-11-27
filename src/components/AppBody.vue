<script>
import { store } from "./store";
import AppCard from "./AppCard.vue";

export default {
  components: {
    AppCard,
  },
  data() {
    return {
      store,
    };
  },
};
</script>
<template>
  <body class="">
    <div class="container d-flex justify-content-center p-3">
      <div class="col d-flex justify-content-center flex-wrap">
        <h2>Found</h2>
        <AppCard v-for="item in store.cardsGet" :list="item" />
      </div>
    </div>
  </body>
</template>
<style scoped lang="scss">
body {
  background-color: orange;
}
.container {
  //   height: 1000px;
  width: 100%;

  .col {
    height: 100%;
    background-color: white;
    gap: 2rem;
    padding-bottom: 4px;

    h2 {
      width: 100%;
      background-color: black;
    }
    .card {
      width: calc(100% / 5);
    }
  }
}
</style>
