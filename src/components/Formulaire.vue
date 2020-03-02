<template>
    <form @submit.prevent="ajouter">
        <div class="row">
            <div class="col-sm-3">
                <label for="nom">Nom :</label>
            </div>
            <div class="col-sm-3">
                <label for="valeur">Valeur :</label>
            </div>
            <div class="col-sm-3">
                <label for="categorie">Catégorie :</label>
            </div>
        </div>
        <div class="row">
            <div class="col-sm-3">
                <input type="text" class="form-control" id="nom" v-model="nom" />
            </div>
            <div class="col-sm-3">
                <input type="number" class="form-control" id="valeur" v-model="valeur" />
            </div>
            <div class="col-sm-3">
                <select class="form-control" id="categorie" v-model="categorie">
                    <option
                        v-for="(valeur, cle) in this.categories"
                        :key="cle"
                        :value="cle"
                    >{{ valeur }}</option>
                </select>
            </div>
            <div class="col">
                <button type="submit" class="btn btn-primary btn-block">ajouter</button>
            </div>
        </div>
    </form>
</template>

<script>
import Objet from "../model/objet";
import { Categories } from "../model/categories";

export default {
    name: "Formulaire",
    data() {
        return {
            nom: "",
            valeur: 0,
            categorie: null,
            categories: Categories
        };
    },
    mounted() {},
    methods: {
        ajouter() {
            console.log(this.nom);
            console.log(this.valeur);
            console.log(Categories[this.categorie]);
            this.$emit("ajout", new Objet(this.nom, this.valeur, Categories[this.categorie]));
        }
    }
};
</script>

<style>
</style>
