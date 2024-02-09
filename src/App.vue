<script >
export default{
  name:'App',
  data(){
    return {
      message:"sarah",
      background:'pink',
      movie:"",
      show: true,
      films:['Matrix','Avatar','Drive'],
      users:[
        {
          id: 1 ,
          name: "giuseppe",
        },
        {
          id: 2 ,
          name: "luca",
        },
        {
          id: 3,
          name: "isabella",
        }
      ]
     }
  },
  methods:{
    greetings(){
      console.log( " ciao" , this.message );
     document.getElementById('emptyEl').innerHTML += `ciao ${this.message}`
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
   <p id="emptyEl"></p>

   <!--loop in array di stringhe -->
   <ul>
    <li v-for="film in films"> 
       {{ film }}
    </li>
   </ul>

   <!--loop in array of object-->
   <ul>
    <li v-for="user in users"> 
       {{ user.name }} : {{ user.id }}
    </li>
   </ul>
  </div>

  <ul>
    <li v-for="n in 10"> {{ n }}</li>
  </ul>
  
</template>
 
<style >

</style>
