<template>
  <main>

      <MainContent
      />
    <h1>{{ searchString }}</h1>
  </main>
</template>

<script>
import axios from "axios"
import MainContent from './MainContent.vue'
export default {
    name:"MainIndex",

    props:{ 'searchString' : String},

    components:{
        MainContent,
    },

    data: function(){
        return{
            
            films: null,

            titolo: null,
            titoloOriginale: null,
            voto: null,
            lingua: null,
        }
    },

    created: function(){
        this.apiFilms()
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
    }

    
}
</script>

<style lang="scss" scoped>
    main{
        background-color: grey;
        height: 90vh;
    }
</style>