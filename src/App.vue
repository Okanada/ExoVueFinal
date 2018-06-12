
<template>
<div id="app">
    <!-- Début instance -->
  <body>
    <h1 class="titrebody text-center pt-5"> VUE.JS - EXO</h1>
    <div class="row pt-5 pb-5 justify-content-around" id="MesBoutons">
        <a class="btn btn-primary active" href="#" role="button" data-position="1" @click.prevent="clickBtn">Exo1</a>
        <a class="btn btn-primary" href="#" role="button" data-position="2" @click.prevent="clickBtn">Exo2</a>
        <a class="btn btn-primary" href="#" role="button" data-position="3" @click.prevent="clickBtn">Exo3</a>
        <a class="btn btn-primary" href="#" role="button" data-position="4" @click.prevent="clickBtn">Exo4</a>
        <a class="btn btn-primary" href="#" role="button" data-position="5" @click.prevent="clickBtn">Exo5</a>
        <a class="btn btn-primary" href="#" role="button" data-position="6" @click.prevent="clickBtn">Exo6</a>
        <a class="btn btn-primary" href="#" role="button" data-position="7" @click.prevent="clickBtn">Exo7</a>
        <a class="btn btn-primary" href="#" role="button" data-position="8" @click.prevent="clickBtn">Exo8</a>
        <a class="btn btn-primary" href="#" role="button" data-position="9" @click.prevent="clickBtn">Exo9</a>
        <a class="btn btn-primary" href="#" role="button" data-position="10" @click.prevent="clickBtn">Exo10</a>
    </div> 
  
 

    <div class="container">
        <exo1 v-show="isActive == 1"/>
        <exo2 v-show="isActive == 2"/>
        <exo3 v-show="isActive == 3"/>
        <exo4 v-show="isActive == 4"/>
        <exo5 v-show="isActive == 5"/>
        <exo6 v-show="isActive == 6"/>
        <exo7 v-show="isActive == 7"/>
        
    </div>
  </body>
</div>
  <!-- C'est le html que l'on va mettre dans le template -->
</template>





<script>
import exo1 from "./components/exo1.vue";
import exo2 from "./components/exo2.vue";
import exo3 from "./components/exo3.vue";
import exo4 from "./components/exo4.vue";
import exo5 from "./components/exo5.vue";
import exo6 from "./components/exo6.vue";
import exo7 from "./components/exo7.vue";

export default {
  name: "approot",
  data() {
    return {
      isActive: 7
    };
  },

  methods: {
    clickBtn(event) {
      this.isActive = event.target.dataset.position;
    }
  },
  components: { exo1, exo2, exo3, exo4, exo5, exo6, exo7 }
};
</script>






<style lang="scss">
@import "./assets/sass/main.scss";
</style>

<style scoped lang="scss">
body {
  background-image: url("../src/img/piratas-sombrero-paja.jpg");
  padding-bottom: 500px;
}

.titrebody {
  color: tomato;
}
</style>
