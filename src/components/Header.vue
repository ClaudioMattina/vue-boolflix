<template>
    <header>

        <div>
            <h2>BoolFix</h2>
            <h2>{{ricerca}}</h2>
            <h1>{{titolo}}</h1>
        </div>
        <div id="inputs">
            <input v-model="ricerca" type="text">
        
        <a href="">Search</a>
        </div>
        
    </header>
</template>

<script>


import axios from "axios"
export default {
    name: "HeaderIndex",

    data: function(){
        return{
            ricerca:"",
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
            axios.get("https://api.themoviedb.org/3/movie/550?api_key=5f9d6c871c535668747bc3410bc15999&query=ritorno+al+futuro").then((result) =>{
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
    header{
        height: 10vh;
        background-color: black;
        color: white;
        display: flex;
        align-items: center;
        justify-content: space-between;
        
        
            input{
                height: 20px;
                width: 200px;
            }

            a{
                margin: 0 20px;
                color: white;
                text-decoration: none;
                border: 1px solid blue;
                padding: 10px 20px;
                background-color: blue;
            }

            h2{
                margin-left: 20px;
            }
    }
</style>