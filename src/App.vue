<template>
  <div id="app">
    <Formulaire/>
    <Tableau/>
    <Graphiques/>
  </div>
</template>

<script>
import Formulaire from './components/Formulaire'
import Tableau from './components/Tableau'
import Graphiques from './components/Graphiques'

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
