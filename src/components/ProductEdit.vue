<template>
    <form class="marg center margt" @submit="valid">
        <div class="center">
            <label for="titre">Inscrivez le titre : </label>
            <input class="margr" type="text" name="titre" id="titre" minlength="3" maxlength="50" required>
            <label for="categorie">Choisissez une catégorie : </label>
            <select name="categorie" id="categorie" required>
                <option v-for="categorie in categories" v-bind:categorie="categorie" v-bind:key="categorie.id">{{categorie.title}}</option>
            </select>
        </div>
        <div class="margt">
            <button type="submit">Cliquez ici pour soumettre la modification</button>
        </div>
    </form>
</template>

<script>

export default {
    name: "ProductEdit",
    props: {
        categories: Array,
    },
    methods: {
    valid: function () {
        alert("Le titre a été ajouté");
    },
    },
};

</script>

<style scoped>

    .margr {
        margin-right: 5em;
    }

    .margt {
        margin-top: 3em;
    }

    .center {
        text-align: center;
    }
</style>