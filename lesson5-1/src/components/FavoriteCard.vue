<template>
  <div class="container">
    <div class="img">
      <img :src="cardData.img" class="img" />
    </div>
    <div class="title">
      <div class="icon" :style="{ backgroundColor: cardData.icon }"></div>
      <div>
        <a target="_blank" :href="cardData.link">{{ cardData.title }}</a>
      </div>
      <div class="stock">{{ cardData.stock }}</div>
    </div>
    <div class="discription">{{ cardData.discription }}</div>
  </div>
</template>

<script>
export default {
  name: "FavoriteCard",

  props: {
    cardData: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style lang="css" scoped>
.container {
  display: inline-block;
  width: 120px;
  height: 190px;
  border: 2px solid black;
  overflow: hidden;
}
.icon {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background-color: gray;
}
.img {
  width: 120px;
  height: 130px;
}
.title {
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  gap: 3px;
  font-size: 9px;
  width: 90px;
}
.stock {
  color: green;
}
.discription {
  font-size: 9px;
}
</style>
