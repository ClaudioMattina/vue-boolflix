<template>
  <main>

      <MainContent
      />

  </main>
</template>

<script>
import MainContent from './MainContent.vue'
export default {
    name:"MainIndex",
    components:{
        MainContent
    }
}
</script>

<style lang="scss" scoped>
    main{
        background-color: grey;
        height: 90vh;
    }
</style>