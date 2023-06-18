<template>
  
  
  <navBar/>
  <dashBoard/>
  <mainContent></mainContent>
  
</template>

<script>

import navBar from './components/navBar.vue'
import dashBoard from './components/dashBoard.vue'
import mainContent from './components/mainContent.vue';


export default {
  name: 'App',
  components: {
    
    navBar,
    dashBoard,
    mainContent
    
  }
}
</script>

<style>


@import './assets/css/styles.css';
</style>

