<template>
  <div class="container">
    <div class="img">
      <img :src="cardLeptop.foto" class="img" />
    </div>
    <div class="data">
      <div>
        <a class="title" href="cardLeptop.link">{{ cardLeptop.title }}</a>
      </div>

      <p class="saving">
        <span class="text">Ваша економiя</span>
        {{ cardLeptop.oldPrice - cardLeptop.newPrice }} грн.
      </p>

      <div class="old-price">{{ cardLeptop.oldPrice }} грн.</div>
      <div class="new-price">{{ cardLeptop.newPrice }}грн.</div>
      <button class="button">Kупити</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "LeptopsCard",
  props: {
    cardLeptop: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style lang="css" scoped>
.container {
  display: flex;
  justify-content: space-between;
  gap: 5px;
  width: 250px;
  height: 130px;
  border: 2px solid black;
}
.img {
  width: 70px;
  height: 130px;
}
.data {
  display: inline-block;
}
.saving {
  color: red;
  font-size: 9px;
}
.old-price {
  text-decoration: line-through;
  color: grey;
  font-size: 10px;
}
.new-price {
  color: red;
  font-size: 16px;
}
.button {
  width: 60px;
  height: 25px;
  color: white;
  background-color: green;
  margin-left: 110px;
  font-size: 10px;
}
.text {
  font-size: 9px;
  color: black;
}
</style>
