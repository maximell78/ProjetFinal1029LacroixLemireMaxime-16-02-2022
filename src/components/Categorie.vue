<template>
    <div>
        <h1>{{categorie.title}}</h1>
    </div>
</template>

<script>

export default {
    name: "Categorie",
    props: {
        categorie: {
            title: String,
        },
    },
};
</script>
