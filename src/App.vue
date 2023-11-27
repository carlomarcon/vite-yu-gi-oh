<script>
import Appheader from "./components/Appheader.vue";
import AppBody from "./components/AppBody.vue";
import AppFooter from "./components/AppFooter.vue";
import axios from "axios";

export default {
  components: {
    Appheader,
    AppBody,
    AppFooter,
  },
  created() {
    axios.get().then();
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
