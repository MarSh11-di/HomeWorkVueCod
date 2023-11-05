<template>
  <div>
    <favorite-card
      v-for="card in cardDataList"
      :key="card.id"
      :card-data="card"
    />
  </div>
</template>

<script>
import FavoriteCard from "./FavoriteCard.vue";

export default {
  name: "FavoritBlock",
  components: { FavoriteCard },
  props: {
    cardDataList: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss" scoped></style>
