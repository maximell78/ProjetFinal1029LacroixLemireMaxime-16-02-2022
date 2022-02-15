<template>
    <form class="marg center">
        <h1>Formulaire de contact</h1>
        <div class="center">
            <label for="lname">Votre nom : </label>
            <input class="margr" type="text" name="lname" id="lname" placeholder="Lacroix-Lemire" required>
            <label for="lname">Votre prénom : </label>
            <input type="text" name="lname" id="fname" placeholder="Maxime" required>
        </div>
        <br/>
        <div class="center">
            <label for="email">Votre courriel : </label>
            <input class="margr" type="email" name="email" id="email" placeholder="max@maximal.ca" pattern="[a-zA-Z]+[\@]{1,1}[a-zA-Z]+[\.]{1,1}[a-zA-Z]{2,3}+/g" required>
            <label for="categorie">Choisir une catégorie : </label>
        <select name="categorie" id="categorie" required>
            <option v-for="categorie in categories" v-bind:categorie="categorie" v-bind:key="categorie.id">{{categorie.title}}</option>
        </select>
        </div>
        <div class="center margt">
            <button type="submit">Cliquez ici pour soumettre</button>
        </div>        
    </form>
</template>

<script>

export default {
    name: "Contact",
    props: {
        categories: Array,
    },
};
</script>

<style scoped>

    .marg{
        margin: 5em;
    }

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