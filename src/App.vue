<script setup>
  import Navbar from './components/Navbar.vue';
  import jumbotron from './components/jumbotron.vue';
</script>

<template>  
  <header>
    <Navbar/>
  </header>
  <main>
    <jumbotron/>
  </main>
  <main></main>
</template>

<style scoped>
  main {
    height: 20000px;
  }
</style>
