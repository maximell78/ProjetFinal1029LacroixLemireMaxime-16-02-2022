<template>
    <div class="card">
        <h1>{{product.title}}</h1>
        <p class="categorie">{{product.categorie}}</p>
    </div>
</template>

<script>

export default {
    name: "Product",
    props: {
        product: {
            title: String,
            categorie: String,
        },
    },
};
</script>
