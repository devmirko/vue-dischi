<template>
  <div id="app">
    <HeaderApp/>
    <main>
      <SelectedOption/>
      <MainCard/>
    </main>
    
  </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue'
import MainCard from './components/MainCard.vue'
import SelectedOption from './components/SelectedOption.vue'

export default {
  name: 'App',
  components: {
    HeaderApp,
    MainCard,
    SelectedOption
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

</style>
