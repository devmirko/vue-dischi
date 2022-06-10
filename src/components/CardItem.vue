<template>
<div class="card">
    <div class="box_image">
        <img :src="listObject.poster" :alt="listObject.title">
    </div>
    <div class="box_text">
        <h3>{{listObject.title}}</h3>
        <span>{{listObject.author}}</span><br>
        <span>{{listObject.year}}</span>
    </div>
   

</div>


</template>

<script>
export default {
 name: 'CardItem',
 props: {
    listObject: Object
   
 }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.card{
    flex-basis: calc( 100% / 5 );
    height: 200px;
}


</style>