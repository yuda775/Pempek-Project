<script setup>
  import Navbar from './components/Navbar.vue';
  import Jumbotron from './components/Jumbotron.vue';  
  import Marketplace from './components/Marketplace.vue';
  import TentangKami from './components/TentangKami.vue';
  import Menu from './components/Menu.vue';
  import TestimoniCard from './components/TestimoniCard.vue';
</script>

<template>  
  <header>
    <Navbar/>
  </header>
  <main>    
    <section id="beranda">
      <Jumbotron/>      
    </section>
    <Marketplace/>
    <section id="tentang-kami">
      <TentangKami/>
    </section>
    <section id="menu">
      <!-- <Menu/> -->
    </section>
    <section id="testimoni">
        <div class="container">
      <h1 class="mt-4 mb-4">Testimoni</h1>
      <div class="row">
        <div class="col-md-4">
          <img src="assets/images/adaan.png" alt="">
          <TestimoniCard
            profilePhoto="assets/images/adaan.png"
            username="john.doe"
            description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque et mauris ut turpis efficitur viverra."
          />
        </div>
        <div class="col-md-4">
          <TestimoniCard
            profilePhoto="path_to_profile_photo_2.jpg"
            username="jane.smith"
            description="Curabitur in enim ut mi rutrum volutpat vitae nec mi. Ut aliquet, ipsum a scelerisque tincidunt, lectus orci euismod lacus."
          />
        </div>
        <div class="col-md-4">
          <TestimoniCard
            profilePhoto="path_to_profile_photo_3.jpg"
            username="alex.williams"
            description="Vivamus fermentum nulla non ligula auctor, vel tristique est cursus. Donec eleifend ipsum et condimentum tristique."
          />
        </div>
      </div>
    </div>
    </section>
  </main>
</template>

<style scoped>
  main {
    height: 20000px;
  }
  
</style>
