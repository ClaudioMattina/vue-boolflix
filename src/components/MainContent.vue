<template>
  <div class="scheda">
    <h5> {{infoOggetti.original_title}} </h5>
    <p>titolo originale</p>
    <p>lingua</p>
    <p>voto</p>
  </div>
</template>

<script>

export default {
    name:"MainContentIndex",
    props: {"infoOggetti" : Object,},
    
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
  }
</style>