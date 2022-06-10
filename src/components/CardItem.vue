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
    width: calc(100% / 5 - 30px );
    height: 450px;
    margin-left: 30px;
    margin-bottom: 20px;
    background-color: #2E3A46;
     
         .box_image{
            width: 100%;
            height: 70%;
            
            
            

              img{
                width: 100%;
                height: 100%;
                padding: 30px;
              }
         }

         .box_text{
            width: 100%;
            height: 50%;
            text-align: center;

            h3{
                margin: 10px 0;
                color: white;
                font-size: 24px;
                font-weight: 700
            }

            span{
                color: dimgray;
                font-size: 24px;
                
            }
         }
}


</style>