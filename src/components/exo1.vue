<template lang="html">

 <div class="row pt-5 panel">

  <div id="exo1" class="col-6 bg-primary pt-5">

    <h1 v-if="affichage">ceci est mon titre</h1>
    <button @click.prevent="test">Show</button>

  </div>
</div>
</template>



<script lang="js">
  export default  {
    name : "exo1",
    data() {
        return {
            affichage: true
        }
    },

    methods: {
        test() {
            
            this.affichage = !this.affichage

        },
    }
}
</script>

<style scoped lang="scss">

</style>
