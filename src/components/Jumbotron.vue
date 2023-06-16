<script setup>
import VectorJumbotron from './icons/WavesJumbotron.vue';
</script>

<template>    

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