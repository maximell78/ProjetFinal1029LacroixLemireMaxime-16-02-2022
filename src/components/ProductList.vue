<template>
    <div>
        <product v-for="product in products" v-bind:product="product" v-bind:key="product.id"></product>
        <product-edit :product="products[0]"></product-edit>
    </div>
</template>

<script>
import ProductEdit from "./ProductEdit.vue";
import Product from "./Product.vue";

export default {
    name: "ProductList",
    components: {
        ProductEdit,
        Product,
    },
    props: {
        products: Array
    },
    methods: {
        showValues: function() {
            alert(
                `Titre du produit: ${this.monproduit.title} Produit: ${this.monproduit.product}`
            );
        },
    },
};
</script>