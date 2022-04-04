<template>
  <div id="app">


    <Header @search="ricercaAxios"/>

    <Main :searchString="oggetto" />

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
      oggetto: null,


      films: null,

      titolo: null,
      titoloOriginale: null,
      voto: null,
      lingua: null,
    }
  },

  methods:{

       apiFilms(){
            axios.get("https://api.themoviedb.org/3/movie/550?api_key=5f9d6c871c535668747bc3410bc15999&query=").then((result) =>{
                this.titolo = result.data.name
                this.titoloOriginale = result.data.original_title
                this.voto = result.data.popularity
                this.lingua = result.data.original_language
                
            })
        }
    },

    ricercaAxios(textToSearch){
      /* console.warn(inputText) */
      this.oggetto = `https://api.themoviedb.org/3/movie/550?api_key=5f9d6c871c535668747bc3410bc15999&query=${textToSearch}` 
    }
  }

</script>

<style lang="scss">
    #app{
     
    }
</style>
