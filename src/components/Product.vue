<template>
    <div class="card">
        <h1><categorie v-for="categorie in categories" v-bind:categorie="categorie" v-bind:key="categorie.id"></categorie></h1>
        <p class="categorie">{{product.name}}</p>
    </div>
</template>

<script>
import Categorie from "./Categorie.vue";

export default {
    name: "Product",
    components: {
        Categorie,
    },
    props: {
        product: {
            name: String,
        },
        categories: Array,
    },
};
</script>
