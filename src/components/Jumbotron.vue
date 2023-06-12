<script setup>
import VectorJumbotron from './icons/WavesJumbotron.vue';
</script>

<template>    
<div class="position-relative overflow-x-hidden"> 
  <div class="container">
    <div class="jumbotron row align-items-center z-2">
      <div class="title col-lg-6">
        <h1 class="headline-1">Cari Makanan Tradisional <br> Palembang ?</h1>
        <p class="lead">Pempek Princess jawabannya, Asli <br> buatan orang Palembang</p>
        <a class="link" href="#menu">View Our Menu</a>
      </div>
      <div class="col-lg-6 mt-5" style="filter: drop-shadow(2px 2px 70px rgba(0, 0, 0, 0.25));">
        <img src="./icons/PempekJumbotron.png" alt="">    
      </div>
    </div>  
  </div>
  <div class="vector-jumbotron">
    <VectorJumbotron/>  
  </div>
</div>
</template>


<style>
.jumbotron {
  position: relative;
  padding-top: 100px;  
  padding-bottom: 200px;
  justify-content: space-evenly;  
  z-index: 1;   
}

.headline-1 {
  font-size: 42px;
  font-weight: 700;
  color: var(--secondary-color);
  border-left: 10px solid var(--primary-color);
  padding-left: 10px;
}

.link {
  padding: 10px 25px;
  background-color: var(--primary-color);
  color: white;
  text-decoration: none;
  font-weight: 700;
  border-radius: 20px;
}

.vector-jumbotron {
  position: absolute;  
  top: 0px;
  right: 0px;  
  z-index: 0;
}

@media (max-width: 767.98px) {
  .headline-1 {
    font-size: 32px;
    border-left: 5px solid var(--primary-color);
  }

  .lead {
    font-size: 16px;
  }

  .link {
    font-size: 12px;
  }

  .vector-jumbotron {
    position: absolute;
    top: 80px;
    right: -450px;          
  }

}

</style>