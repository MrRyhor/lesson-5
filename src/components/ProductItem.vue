<template>
  <div class="container">
    <a :href="itemData.link">
      <div class="img-container">
        <img class="main-image" :src="itemData.imgSrc" alt="product" />
        <div class="label-container">
          <img class="label-image" src="../assets/label.png" alt="label" />
        </div>
      </div>
      <div class="info-container">
        <div class="logo-container">
          <img :src="itemData.logo" alt="logo" />
          <h5>{{ itemData.companyTitle }}</h5>
        </div>
        <div class="stock" v-if="itemData.inStock">В наличии</div>
        <div class="no-stock" v-else>Нет в наличии</div>
      </div>
      <div class="description">{{ itemData.description }}</div>
    </a>
  </div>
</template>
<script>
export default {
  name: "ProductItem",

  props: {
    itemData: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>
<style lang="css" scoped>
a {
  text-decoration: none;
}
.container {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 10px;
}
.img-container {
  background-size: contain;
  object-fit: contain;
  position: relative;
}
.info-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 14px;
}
.info-container img {
  width: 14px;
}
.logo-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  color: #fff;
}
.stock {
  color: rgb(0, 126, 84);
}
.no-stock {
  color: rgb(246, 0, 0);
}
.description {
  text-align: left;
  color: #fff;
  font-size: 18px;
}
.main-image {
  width: 200px;
  height: 200px;
  border-radius: 10px;
}
.label-image img {
  width: 16px;
  
}
.label-container {
  background-color: black;
  opacity: 0.7;
  position: absolute;
  bottom: 10px;
  left: 10px;
  padding: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
}
</style>
