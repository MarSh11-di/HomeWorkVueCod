<template>
  <div>
    <leptops-card
      v-for="leptop in leptopList"
      :key="leptop.id"
      :card-leptop="leptop"
    />
  </div>
</template>

<script>
import LeptopsCard from "./LeptopsCard.vue";
export default {
  name: "LeptopsBlock",
  components: {
    LeptopsCard,
  },
  props: {
    leptopList: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss" scoped></style>
