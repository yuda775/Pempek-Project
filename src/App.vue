<script setup>
  import Navbar from './components/Navbar.vue';
  import Jumbotron from './components/Jumbotron.vue';  
  import Marketplace from './components/Marketplace.vue';
  import TentangKami from './components/TentangKami.vue';
  import Menu from './components/Menu.vue';
</script>

<template>  
  <header>
    <Navbar/>
  </header>
  <main>    
    <Jumbotron/>    
    <Marketplace/>
    <TentangKami/>
    <Menu/>
  </main>
</template>

<style scoped>
  main {
    height: 20000px;
  }
  
</style>
