<template>
  <main>

      <MainContent
      />
    <h1></h1>
  </main>
</template>

<script>

import MainContent from './MainContent.vue'
export default {
    name:"MainIndex",

    props:["searchString"],

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
        height: 90vh;
    }

</style>