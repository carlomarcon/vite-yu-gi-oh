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
      key: "",
    };
  },
  methods: {
    onChange: function () {
      console.log(this.key);
    },
  },
};
</script>
<template>
  <body class="py-4">
    <select
      class="form-select w-25 mx-5"
      aria-label="Default select example"
      @change="onChange($event)"
      v-model="key"
    >
      <option value="Alien">Alien</option>
      <option value="Ally of Justice">Ally of Justice</option>
      <option value="Ancient Gear">Ancient Gear</option>
      <option value="Noble Knight">Noble Knight</option>
    </select>
    <div class="container d-flex justify-content-center p-3">
      <div class="col d-flex justify-content-center flex-wrap">
        <h2>Found {{ store.cardsGet.length }} cards</h2>
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
