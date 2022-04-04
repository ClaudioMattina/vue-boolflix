<template>
  <div class="scheda">
    <h1>Titolo</h1>
    <p>titolo originale</p>
    <p>lingua</p>
    <p>voto</p>
  </div>
</template>

<script>
export default {
    name:"MainContentIndex"
}
</script>

<style lang="scss" scoped>
  .scheda{
    background-color: white;
    height: 200px;
    width: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
</style>