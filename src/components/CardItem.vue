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
    width: 15%;
    height: 350px;
    margin-left: 10px;
    background-color: #2E3A46;
     
         .box_image{
            width: 100%;
            height: 50%;
            

              img{
                width: 100%;
                height: 100%;
              }
         }

         .box_text{
            width: 100%;
            height: 50%;
            text-align: center;
         }
}


</style>