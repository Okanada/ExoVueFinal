<template lang="html">

<div class="container panel">
  <div class="row parentsbg pt-5">
    
      <div v-if="toggle1" class="col-5 bg-anakinyoung">

         <h3 class="pt-5 pb-5 text-warning">
         May the force
         </h3>

      </div>
    
     
      <div v-if="!toggle1" class="col-5 bg-anakinold">
        <h3 class="pt-5 pb-5 text-warning">
         Be With You
         </h3>  
      </div>

  </div>


  <center>
    <button @click.prevent ="changetoggle" class="boutonchange btn btn-warning" type="submit">Light or Dark</button>
  </center>
 
</div>
 
</template>





<script lang="js">
  export default  {
    name : "exo4",
    data() {
      return{
        toggle1 : true,
      
        
      }
    },

    methods: {
        changetoggle() {
            
            this.toggle1 = !this.toggle1

        },
    }

  
}
</script>




<style lang="scss" scoped>
.parentsbg {
  position: relative;
}

.bg-anakinyoung {
  background-image: url("./../img/younganakin.jpg");
  background-size: 100%;
  background-repeat: no-repeat;

  border-radius: 25px;
}

.bg-anakinold {
  background-image: url("./../img/anakin_skywalker_2.jpg");
  background-size: 100%;
  background-repeat: no-repeat;
  border-radius: 25px;
  position: absolute;
  right: 0px;
}

.boutonchange {
  position: absolute static;
}
</style>



