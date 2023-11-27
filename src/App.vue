<script>
import Appheader from "./components/Appheader.vue";
import AppBody from "./components/AppBody.vue";
import AppFooter from "./components/AppFooter.vue";
import axios from "axios";
import { store } from "./components/store";

export default {
  components: {
    Appheader,
    AppBody,
    AppFooter,
  },
  data() {
    return {
      // cardsGet: [],
      store,
    };
  },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((resp) => {
        this.store.cardsGet = resp.data.data;
        console.log(this.store);
      });
  },
};
</script>

<template>
  <Appheader />
  <AppBody />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
