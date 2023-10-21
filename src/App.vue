<template>
  <products-list :products-list-data="raspberryList"/>
</template>

<script>
import ProductsList from "./components/ProductsList.vue";
import { raspberryList } from "./constants/2_data_raspberry";

export default {
  name: "App",
  components: {
    ProductsList,
  },

  data() {
    return {
      raspberryList,
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
  background-color: rgb(31, 31, 31);
  max-width: 680px;
  margin: 0 auto;  
}
</style>
