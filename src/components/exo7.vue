<template lang="html">
<!-- Exercice 7 -->
  <section>
   <h3 class="text-primary mx-auto ">
    To Do List
   </h3>
   
   <div class="row bg-primary pt-5 pb-5" id="rowtodolist">
      <input v-model="inputtache" class="form-control col-9 mt-5" type="text" placeholder="Accompli ta tâche" id="nametask">
      <button @click="addTask" type="button" class="btn btn-dark mt-5 col-3" id="btnok">OK</button>
   </div>

   <button type="button" class="btn btn-success mt-5" id="btnall">All</button>
   <button type="button" class="btn btn-success mt-5" id="btntodo">To Do</button>
   <button type="button" class="btn btn-success mt-5" id="btndone">Done</button>

   <div class="tasklist pt-5">
     <taskbar v-for="(element,index) in poche" :key="index" :message="element"/>
   </div> 
  
  
  </section>
            <!-- Fin exercice 7 -->
</template>





<script lang="js">
import taskbar from "./BarreDeTâche"
  export default  {
    name: 'exo7',   
    data() {
      return {
        input : "",
        inputtache:"",
        poche : [],
       
        
        

      }
    },

    components : {taskbar},

    methods : {
      addTask(){
        
        this.poche.push({text : this.inputtache});
          this.inputtache = "";

        
        
      },
      
      
    },
  
  }
  
 

</script>







<style scoped lang="scss">
#rowtodolist {
  border-radius: 25px;
}
</style>
