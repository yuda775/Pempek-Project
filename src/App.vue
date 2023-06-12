<script setup>
  import Navbar from './components/Navbar.vue';
  import Jumbotron from './components/Jumbotron.vue';  
  import Marketplace from './components/Marketplace.vue';
  import TentangKami from './components/TentangKami.vue';
  import Menu from './components/Menu.vue';
  import TestimoniCard from './components/TestimoniCard.vue';  
  import TestimoniCardLarge from './components/TestimoniCardLarge.vue';
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
      <Menu/>
    </section>
    <section id="testimoni">    
    <div class="container">
      <h2 class="mt-4 mb-3 text-center headline-2">Testimoni</h2>
      <div class="line"></div>
      <div class="cards row mt-5 align-items-center">
        <div class="col-md-4">    
          <div class="d-flex justify-content-center px-5">            
              <TestimoniCard
              profilePhoto="src/assets/images/profile/aldi.jpg"
              username="@john.doe"
              description="Maaci umi kirimannya, ini pempek kates yang bisa dikirim ke jakarta yang isinyo aman dan masih seger. mantabb"
              />            
          </div>
        </div>
        <div class="col-md-4">
          <div class="d-flex justify-content-center">           
              <TestimoniCardLarge
              profilePhoto="src/assets/images/profile/aldi.jpg"
              username="@jane.smith"
              description="Alhamdulillah, Laksana nyo nyampe sebelum buko plus bonus talam ubi ungu, baik banget mevaah, mokaseh @pempek_princess. “maka nikmat Tuhan manalagi yg kau dusta”"
              />            
          </div>
        </div>
        <div class="col-md-4">
          <div class="d-flex justify-content-center px-5">            
              <TestimoniCard
              profilePhoto="src/assets/images/profile/aldi.jpg"
              username="@alex.williams"
              description="Pempek Princess, lezatnya sebuah pempek tak hanya memiliki cita rasa enak dilidah saja, tetapi juga perpaduan bumbu yang menggugah selera serta membuat ketagihan."
              />            
          </div>
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
