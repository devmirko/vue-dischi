<template>
<div class="container">
    <select  v-model="selected"
    @change ="$emit('mySearch', selected)">
        <option value="all">all</option>
        <option value="pop">pop</option>
        <option value="rock">rock</option>
        <option value="jazz">jazz</option>
        <option value="metal">metal</option>
    </select>
    <span> Hai selezionato : {{ selected }}</span>



</div>


</template>

<script>
export default {
 name: 'SelectedOption',
  data() {
    return {
      selected: ''
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
    height: 100%;
    display: flex;
    justify-content: center;
    background-color: #1E2D3B;
    align-items: center;

     select{
        width: 100px;
        margin-right: 20px;
     }
     span{
        color: white;
        font-size: 20px;
        font-weight: 700;
     }
}



</style>