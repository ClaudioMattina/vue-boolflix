<template>
  <main>

      

      <MainContent v-for="(element, index) in oggettiTrovati" :key="index"
      :infoOggetti = "element"
      :urlImg = "element.poster_path"
      />

    
  </main>
</template>

<script>

import MainContent from './MainContent.vue'
export default {
    name:"MainIndex",

    props:["oggettiTrovati",],

    components:{
        MainContent,
    },

    data: function(){
        return{
               
            
        }
    },

    created: function(){
       
    },

    methods:{
     
    }
    
}
</script>

<style lang="scss" scoped>

    main{
        background-color: grey;
        
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 5px;
        padding: 50px 10px;
    }

</style>