<template>
<header>
    <img src="../assets/logo-small.svg" alt="questa è un immagine">
 
</header>  
</template>

<script>
export default {
  name: 'HeaderApp',
  components: {
   

  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header{
    width: 100%;
    height: 75px;
    background-color: #2E3A46;
    display: flex;
    justify-content: start;
    align-items: center;

    img{
        width: 50px;
        height: 50px;
        margin-left: 10px;
    }
}
   

</style>
