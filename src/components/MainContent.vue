<template>
      
      <div class="card" style="width: 18rem;">
          <img :src="`http://image.tmdb.org/t/p/w500/${infoOggetti.poster_path}`" class="card-img-top" alt="">
          <div class="card-body">
                <h5 class="card-title"> {{infoOggetti.original_title}} {{infoOggetti.name}} </h5>
                <p class="card-text"> <lang-flag :iso="`${infoOggetti.original_language}`" /> </p>
                <p class="card-text"> {{infoOggetti.vote_average}} </p>
          </div>
      </div>
    
  
</template>

<script>

export default {
    name:"MainContentIndex",
    props: {"infoOggetti" : Object},
    
    data: function(){
      return{
       
      }
    },

    
}

</script>


<style lang="scss" scoped>
  .scheda{
    text-align: center;
    background-color: white;
    height: 200px;
    width: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 50px 5px;
  }
</style>