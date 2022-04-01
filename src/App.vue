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
      string:"",
    }
  },

  methods:{
    ciao(input){
      console.warn(input)
      this.string = input
    }
  }
}
</script>

<style lang="scss">
    #app{
     
    }
</style>
