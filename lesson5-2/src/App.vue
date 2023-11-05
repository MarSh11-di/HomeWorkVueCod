<template>
  <leptops-block :leptop-list="leptopsData" />
</template>

<script>
import LeptopsBlock from "./components/LeptopsBlock.vue";
import { leptopsData } from "./constans/data_nout";

export default {
  name: "App",
  components: {
    LeptopsBlock,
  },
  data() {
    return {
      leptopsData,
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
