<template>
  <div id="app">
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{actor.name}}</h2>
      <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
      <h1 v-for="(value,key,index) in myInfo" :key="value">{{index}} {{key}} {{value}}</h1>
    </div>

    <div v-for="name in names" :key="name">
      <h2>{{name}}</h2>
      <hr>
    </div>
    </div>
    
</template>

<script>
export default {
  data() {
    return {
        names: ['John', 'Jane', 'Jack'],
      
      actors:[
        {name:'cristian bale',
        movies:['batman','superman','ironman']
        },
        {name:'james bond',
        movies:['spy','skyfall','casino royale']
        },
        {name:'tom hanks',
        movies:['tom hanks','tom hanks','tom hanks']
        }
      ] ,
      myInfo:{
        name:'cristian bale',
        // channels:['batman','superman','ironman'],
        channels:'code',
        course:"vue3"
         
      }

};
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
