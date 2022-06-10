<template>
<div class="card">
    <div class="box_image">
        <img :src="img" :alt="title">
    </div>
    <div class="box_text">
        <h3>{{title}}</h3>
        <span>{{author}}</span><br>
        <span>{{year}}</span>
    </div>
   

</div>


</template>

<script>
export default {
 name: 'CardItem',
 props: {
    img: String,
    author: String,
    title: String, 
    year: String,
   
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