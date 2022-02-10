<template>
  <div id="app">
    <headerA></headerA>
    <hr>
    <product-list v-bind:products="products"></product-list>
    <footerA></footerA>
  </div>
</template>

<script>
import ProductList from "./components/ProductList.vue";
import FooterA from "./components/FooterA.vue";
import HeaderA from "./components/HeaderA.vue";

export default {
  name: 'App',
  components: {
    ProductList,
    FooterA,
    HeaderA
  },
  data() {
    return {
      products: [
        {
          id: 1,
          title: "Spider-Man: No way home",
          categorie: "Jeux-Videos",
        },
        {
          id: 2,
          title: "Avengers: End Game",
          categorie: "BluRay",
        },
        {
          id: 3,
          title: "Hulk",
          categorie: "DVD",
        }
      ],
      categories: [
        {
          id: 1,
          name: "Jeux-Videos"
        },
        {
          id: 2,
          name: "Bluray",
        },
        {
          id: 3,
          name: "DVD",
        }
      ]
    }
  }
}
</script>

<style>
  @import './assets/css/style.css';
</style>