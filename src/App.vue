<template>
  <div id="app">
    <headerA></headerA>
    <hr>
    <product-list v-bind:products="products"></product-list>
    <product-edit v-bind:categories="categories"></product-edit>
    <contact v-bind:categories="categories"></contact>
    <footerA></footerA>
  </div>
</template>

<script>
import ProductList from "./components/ProductList.vue";
import ProductEdit from "./components/ProductEdit.vue";
import Contact from "./components/Contact.vue";
import FooterA from "./components/FooterA.vue";
import HeaderA from "./components/HeaderA.vue";

export default {
  name: 'App',
  components: {
    ProductList,
    ProductEdit,
    Contact,
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
          title: "Jeux-Videos",
        },
        {
          id: 2,
          title: "BluRay",
        },
        {
          id: 3,
          title: "DVD",
        },
      ],
    };
  },
}
</script>

<style>
  @import './assets/css/style.css';
</style>