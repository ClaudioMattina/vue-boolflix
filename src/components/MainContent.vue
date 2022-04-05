<template>

  <div class="scheda">
    
    <div>
        <h5> {{infoOggetti.original_title}} {{infoOggetti.name}} </h5>
        <p> {{infoOggetti.title}} </p>
        <p> {{infoOggetti.original_language}} </p>
        <p> {{infoOggetti.vote_average}} </p>
    </div>
    
  </div>
</template>

<script>

export default {
    name:"MainContentIndex",
    props: {"infoOggetti" : Object},
    
    
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