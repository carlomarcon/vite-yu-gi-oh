<script>
export default {
  props: {
    list: Object,
  },
};

// [num].card_images[0].image_url
</script>
<template>
  <div class="card">
    <img :src="list.card_images[0].image_url" alt="" />
    <h2>{{ list.name }}</h2>
    <h3>{{ list.race }}</h3>
  </div>
</template>
<style scoped lang="scss">
.card {
  background-color: orange;

  img {
    height: 300px;
    width: 100%;
  }
  h2 {
    color: white;
  }

  h3 {
  }
}
</style>
