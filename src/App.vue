<template>
    <div id="app" class="container">
        <Formulaire @ajout="ajouter"/>
        <Tableau />
        <Graphiques />
    </div>
</template>

<script>
import Formulaire from "./components/Formulaire";
import Tableau from "./components/Tableau";
import Graphiques from "./components/Graphiques";

import { Categories } from "./model/categories";
import Objet from "./model/objet";

export default {
    name: "App",
    components: {
        Formulaire,
        Tableau,
        Graphiques
    },
    data() {
        return {
            objets: []
        };
    },
    mounted() {
        this.objets = [
            new Objet("objet1", 5, Categories.numero1),
            new Objet("objet2", 15, Categories.numero1),
            new Objet("objet3", 12, Categories.numero1),
            new Objet("objet4", 7, Categories.numero2),
            new Objet("objet5", 23, Categories.numero2),
            new Objet("objet6", 9, Categories.numero3)
        ];
	},
	methods: {
		ajouter(objet){
			console.log(objet)
		}
	}
};
</script>
