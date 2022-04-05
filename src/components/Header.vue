<template>
    <header>

        <div>
            
            <h2>BoolFlix</h2>
            
        </div>
        <div id="inputs">
            <input  @keyup.enter="$emit('search', inputText)" v-model="inputText" placeholder="cerca" type="text">
        
            <a @click="$emit('search', inputText)" href="#">
                Search
            </a>
        </div>
        
    </header>
</template>

<script>



export default {
    name: "HeaderIndex",
    
    data: function(){
        return{
            inputText:"",
        }
    }

}
</script>




<style lang="scss" scoped>
    header{
        margin-top: 0;
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