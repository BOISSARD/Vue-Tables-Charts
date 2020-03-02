<template>
  <div id="app" class="container">
    <Formulaire/>
    <Tableau/>
    <Graphiques/>
  </div>
</template>

<script>
import Formulaire from './components/Formulaire'
import Tableau from './components/Tableau'
import Graphiques from './components/Graphiques'

//import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'

export default {
  name: 'App',
  components: {
    Formulaire,
    Tableau,
    Graphiques
  }
}
</script>

<style>



</style>
