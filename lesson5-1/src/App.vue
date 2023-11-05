<template>
  <favorite-block :card-data-list="cards" />
  <card />
</template>

<script>
import FavoriteBlock from "./components/FavoriteBlock.vue";
import { cards } from "./constans/card";

export default {
  name: "App",
  components: { FavoriteBlock },
  data() {
    return {
      cards,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
