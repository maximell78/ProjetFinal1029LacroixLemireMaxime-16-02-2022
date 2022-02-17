<template>
    <div>
        <product v-for="product in products" v-bind:product="product" v-bind:key="product.id"></product>
    </div>
</template>

<script>
import Product from "./Product.vue";

export default {
    name: "ProductList",
    components: {
        Product,
    },
    props: {
        products: Array,
    },    
};
</script>