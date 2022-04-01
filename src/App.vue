<template>
  <div id="app">


    <Header @search="ciao"/>

    <Main :searchString="string" />

  </div>
</template>

<script>

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
      string: null,
    }
  },

  methods:{
    ciao(input){
      console.warn(input)
      this.string = "https://api.themoviedb.org/3/movie/550?api_key=5f9d6c871c535668747bc3410bc15999&query=" + input
    }
  }
}
</script>

<style lang="scss">
    #app{
     
    }
</style>
