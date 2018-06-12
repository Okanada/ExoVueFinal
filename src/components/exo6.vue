<template lang="html">

  <!-- Exercice 6 -->
            <div class="container panel" id="exo6-panel">

          

                    <!-- LEVEL 2 -->
                    <h3 class="text-primary pt-5">Calculatrice</h3>
                    <div class="w-50 m-autp bg-dark" id="fond-calculatrice">

                        <div class="row justify-content-around pt-2">
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre ">7</button>
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre ">8</button>
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre">9</button>
                            <button @click="chooseOperation" type="button" class="btn btn-warning col-3 operation">+</button>
                        </div>

                        <div class="row justify-content-around pt-2">
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre">4</button>
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre ">5</button>
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre">6</button>
                            <button @click="chooseOperation" type="button" class="btn btn-warning col-3 operation">-</button>
                        </div>

                        <div class="row justify-content-around pt-2">
                            <button  @click="addNumber" type="button" class="btn btn-primary col-2 chiffre ">1</button>
                            <button  @click="addNumber" type="button" class="btn btn-primary col-2 chiffre">2</button>
                            <button  @click="addNumber" type="button" class="btn btn-primary col-2 chiffre">3</button>
                            <button @click="chooseOperation" type="button" class="btn btn-warning col-3 operation">/</button>
                        </div>

                        <div class="row justify-content-around pt-2">
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre ">0</button>
                            <button @click="addNumber" type="button" class="btn btn-primary col-2 chiffre ">.</button>
                            <button @click="calculate" type="button" class="btn btn-light col-2 egal">=</button>
                            <button @click="chooseOperation" type="button" class="btn btn-warning col-3 operation">*</button>
                        </div>

                        <div class="row justify-content-around pt-2">
                            <div class="col-2 p-0"></div>
                            <button @click="refresh" type="button" class="btn btn-danger col-2 justify-content-center">C</button>
                            <div class="col-2"></div>
                            <div class="col-2"></div>
                        </div>

                        <input v-model="ecran" type="text" class="nbr mt-5 text-primary" :class="{'border': bordure,'border-danger': bordure}">
                        <div v-model="resultat" class="resultat bg-light mt-2">{{resultat}}</div>
                    </div>




                </center>
            </div>
            <!-- Fin Exercice 6 -->
</template>





<script lang="js">
  export default  {
    name: 'exo6',
    data(){
      return{
        ecran : "",
        resultat : "",
        bordure : false,
        nombre1 : "",
        nombre2 : "",
        operateur : "",
        reponse : ""
      }
    },

    methods : {
      addNumber(){
        this.ecran += event.target.textContent
        this.resultat = ""
        this.bordure = false
      },

      chooseOperation() {
         this.operateur = event.target.textContent
        if (this.ecran == ""){
          this.bordure = true
          this.resultat = "Choose Number"

        }else {
            this.resultat = this.ecran
            this.nombre1 = this.resultat
             this.nombre2 = this.ecran     
            this.ecran = ""}

      },

      calculate() {
        this.nombre2 = this.ecran
       
        switch (this.operateur) {
          case "+":
            this.reponse = parseInt(this.nombre1) + parseInt(this.nombre2)
            break;
          case "-":
          this.reponse = parseInt(this.nombre1) - parseInt(this.nombre2)
            break;
          case "/":
          this.reponse = parseInt(this.nombre1) / parseInt(this.nombre2)
            break;
          case "*":
          this.reponse = parseInt(this.nombre1) * parseInt(this.nombre2)
            break;

          default:
            break;
        }

        this.resultat = this.nombre1 +"  "+this.operateur+"  "+this.nombre2+" "+'='+" "+this.reponse
        this.ecran = ""
       
      },

      refresh() {
        this.ecran = ""
        this.resultat = ""
        this.bordure = false
      }
    }
    
}
</script>




<style scoped lang="scss">
#fond-calculatrice {
  padding-left: 50px;
  padding-right: 50px;
}
</style>
