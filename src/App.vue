<template>
  <div id="app">


    <Header @search="ricercaAxios"/>

    <Main :oggettiTrovati="oggettoFilmSerie" />

  </div>
</template>

<script>

import axios from "axios"
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main,
  },

  data:function(){
    return{
      oggettoFilm: [],
      oggettoSerie: [],
      oggettoFilmSerie: []

    }
  },

  created: function(){
     
  },

  methods:{

       ricercaAxios(textToSearch){
             this.oggettoFilm = axios.get(`https://api.themoviedb.org/3/search/movie?api_key=5f9d6c871c535668747bc3410bc15999&query=${textToSearch}`).then((result) =>{
              console.warn(textToSearch)
               
              this.oggettoFilm = result.data.results;
              console.log(this.oggettoFilm);
                
            })

              this.oggettoSerie = axios.get(`https://api.themoviedb.org/3/search/tv?api_key=5f9d6c871c535668747bc3410bc15999&query=${textToSearch}`).then((result) =>{
              console.warn(textToSearch)
               
              this.oggettoSerie = result.data.results;
              console.log(this.oggettoSerie);
 
              this.oggettoFilmSerie = [...this.oggettoFilm, ...this.oggettoSerie]
              console.warn(this.oggettoFilmSerie)
                
            })

            
            
        }
    },

   
  }

</script>

<style lang="scss">

@import '~bootstrap/scss/bootstrap.scss';
    #app{
     
    }
</style>
