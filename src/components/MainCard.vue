<template>
<div>
   <div class="option">
    <SelectedOption @mySearch="searchGen" />
   </div>
   <main>

        <div id="container">
             <CardItem v-for="(card, i ) in filteredlistAlbum" :key="i"
            :listObject ="card" />
            

        </div>
   </main>
</div>  
</template>

<script>
import axios from "axios"
import CardItem from './CardItem.vue'
import SelectedOption from './SelectedOption.vue'

export default {
  name: 'MainCard',
  components: {
   CardItem,
   SelectedOption

  },
  data(){
    return{
        apiUrl:"https://flynn.boolean.careers/exercises/api/array/music",
        listAlbum : [],
        userSearch: "",
    }
  },
  created(){
      this.getList();
  },
  methods: {
    getList() {
        axios.get(this.apiUrl)
    .then((result) => {
        this.listAlbum = result.data.response;
        console.log(result);
    })
    .catch((error)  => {
       console.log("errore", error);
    })
    },
    searchGen(selectedUser){
        this.userSearch = selectedUser;
        console.log(selectedUser);
    }

  },
  computed: {
    filteredlistAlbum(){
        if (this.userSearch ==="") {
           return this.listAlbum; 
        } else {
       return this.listAlbum.filter(card => {
            return card.genre.toLowerCase().includes(this.userSearch.toLowerCase());
            
       });
        
    } 
  }
 

}

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.option{
    height: 30px;
    background-color: #1E2D3B
}
main{
    background-color: #1E2D3B;
    width: 100%;
    height: calc(100vh - 105px);
    display: flex;
    justify-content: center;
   

    #container{
        width: 80%;
        display: flex;
        align-content: center;
        flex-wrap: wrap;
           
       
    }
}

</style>