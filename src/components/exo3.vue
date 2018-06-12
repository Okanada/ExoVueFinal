<template lang="html">

<div class = "text-primary">
  <p class ="paraexo3">{{message}}</p>
  <input class="inputexo3" type="text" v-model= "message">
</div>

</template>



<script lang="js">
  export default  {
    name : "exo3",
    data() {
      return{
        message : " Je serai le seigneur des pirates"
      }
    }

  
}
</script>

<style scoped lang="scss">
.paraexo3 {
  background-color: black;
  border-radius: 25px;
}

.inputexo3 {
  border-radius : 25px;
}
</style>
