<template>
    <header>

        <div>
            <h2>BoolFix</h2>
            <h2>{{ricerca}}</h2>
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
        }
    },

    methods:{
        apiFilms(){
            axios.get("").then((result) =>{
                this.ricerca = result.data.boh
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