<template>
   <main>
        <div id="container">
             <CardItem v-for="(card, i ) in listAlbum" :key="i"
            :listObject ="card" />

        </div>
   </main>
</template>

<script>
import axios from "axios";
import CardItem from './CardItem.vue'

export default {
  name: 'MainCard',
  components: {
   CardItem

  },
  data(){
    return{
        apiUrl:"https://flynn.boolean.careers/exercises/api/array/music",
        listAlbum : []
    }
  },
  created(){
      this.getList();
  },
  methods: {
    getList() {
        axios.get(this.apiUrl)
    .then((result) => {
        this.listAlbum = result.data;
        console.log(result);
    })
    .catch((error)  => {
       console.log("errore", error);
    })
    }
  }
 

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main{
    background-color: #1E2D3B;
    width: 100%;
    height: calc(100vh - 75px);
    display: flex;
    justify-content: center;
    align-content: center;

    #container{
        width: 80%;
        min-height: 600px;
        margin: 0 auto;
        display: flex;
    }
}

</style>