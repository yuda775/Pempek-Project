<script setup>
  import Navbar from './components/Navbar.vue';
  import Jumbotron from './components/Jumbotron.vue';  
  import Marketplace from './components/Marketplace.vue';
  import TentangKami from './components/TentangKami.vue';
</script>

<template>  
  <header>
    <Navbar/>
  </header>
  <main>    
    <Jumbotron/>    
    <Marketplace/>
    <TentangKami/>
  </main>
</template>

<style scoped>
  main {
    height: 20000px;
  }
  
</style>
