<template>
  <div id="app">
    
    <Search @ricerca="cercaFilm"/>
    <Film :tuttiFilm ='films' />
  </div>
</template>

<script>
import Search from './components/Search.vue';
import Film from "./components/Film.vue";
import axios from "axios"

export default {
  name: 'App',
  components: {
    Search,
    Film
  },
  methods: {
    cercaFilm: function(needle){
      
      
        console.log(needle)
        axios.get(this.apiLink,{
          params: {
            api_key: this.api_key,
            query: needle,
          }
        }).then((risposta)=>{
          this.films = [...risposta.data.results];
          console.log(this.films)
        })
      
      
    }


  },

  data: function(){
    return{
      api_key: "b44f67a7438dbc78b01da40ce05c127a",
      apiLink: 'https://api.themoviedb.org/3/search/movie',
      films : [],
      }
    },
            

}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
