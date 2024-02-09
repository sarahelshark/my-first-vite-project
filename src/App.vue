<script >
export default{
  name:'App',
  data(){
    return {
      message:"sarah",
      background:'pink',
      movie:"",
      show: true,
    }
  },
  methods:{
    greetings(){
      console.log( " ciao" , this.message );
    }

}
}
</script>

<template>
  <h1 :class="background">ciao {{ message }}!</h1> <!--text interpolation-->
  <button @click='greetings'> cliccami per una sorpresa </button>

  <div>
   <label for="movie"> inserisci il titolo di un film:</label>
   <input type="text" id="movie" v-model="movie">
   <p v-if="show">il film inserito: {{ movie }}</p>
   <p v-show="show">il film inserito: {{ movie }}</p>
  </div>
  
</template>
 
<style >

</style>
