<template>
  <div class="container">
    <div class="row">
      <div class="d-flex flex-wrap justify-content-evenly align-items-center flex-wrap mb-2">
        <div class="col-lg-3 col-md-6 col-sm-6 mt-5" v-for="card in cards" :key="card.id">
          <div class="card-menu">
            <img :src="card.image" class="card-img-top" alt="Card Image">
            <div class="card-body mt-3">
              <h3 class="card-title ps-3 fw-bold fs-5">{{ card.title }}</h3>
              <p class="card-text px-3 pt-2">{{ card.description }}</p>
            </div>
            <div class="pb-2">
              <p class="price">{{ card.price }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const expanded = ref(false);

const cards = [
  {
    id: 1,
    title: 'Pempek Lenjer',
    description: 'Lenjer juga tidak memiliki isian apapun, sehinggsa bisa dikatakan sebagai versi original dari pempek.',
    image: '../public/products/lenjer.png',
    price: 'Rp.15.000 / porsi'
  },
  {
    id: 2,
    title: 'Pempek Kerupuk',
    description: 'Pempek Kerupuk, Kriuk kriuk.',
    image: '../public/products/kerupuk.png',
    price: 'Rp.15.000 / porsi'
  },
  {
    id: 3,
    title: 'Pempek Premium',
    description: 'Pempek Princess Premium artinya menggunakan resep dan bahan yang premium. Perbandingan ikan tenggiri dan sagu 1:0,5 ya kawan dan air yang sangat sedikit.',
    image: '../public/products/kemasan.png',
    price: 'Rp.15.000 / porsi'
  },
  {
    id: 4,
    title: 'Cuko Kamu',
    description: 'Cuko Palembang, untuk campuran pempek atau makanan lainnya',
    image: '../public/products/cuko.png',
    price: 'Rp.15.000 / porsi'
  },
];
</script>

