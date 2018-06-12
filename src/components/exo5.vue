
<template lang="html">

<!-- EXERCICE 5 -->
  <div class="container panel">
    <div class="bg-primary" id="exo-5-panel">
        <h2>Générer des éléments du DOM</h2>
        <p>Cliquer sur le bouton ci-dessous pour générer des oeufs.</p>
        <button @click="ajoutOeuf" class="btn btn-success">Ajouter un oeuf</button>
           <div>
             <oeuf v-for="element in panier"/>
           </div>


    </div>
  </div>
<!-- FIN EXERCICE 5 -->
</template>



<script lang="js">
  import oeuf from "./egg.vue"
  export default  {
    name: 'exo5',
    data() {
      return{
        panier: []
      }
    },

    components: {oeuf},

    methods: {
        ajoutOeuf() {
     this.panier.push(oeuf)
        },   
    } 
  }
</script>


<style scoped lang="scss">
#exo-5-panel {
  border-radius: 25px;
  padding: 30px;
}
</style>
