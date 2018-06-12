<template lang="html">

  <section class="barre-de-tache">
    <div class="divdetache pt-3 mt-3">
      {{message.text}}
    </div>
   
  </section>

</template>

<script lang="js">
  export default  {
    name: 'taskbar',
    props: ["message"],

    data() {
      return {
        
        


      }
    },   
}
</script>

<style scoped lang="scss">
.divdetache {
  background-color: whitesmoke;
  border: solid tomato 3px;
  border-radius: 25px;
}
</style>
