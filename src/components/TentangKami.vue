<script setup>
import VectorTentangKami from './icons/tentang-kami.vue';
</script>

<template>
  <div class="position-relative">
    <div class="container position-relative z-1">
      <h2 class="headline-2">Tentang-kami</h2>
      <div class="line"></div>
      <div class="row align-items-center tentangKami-content mt-5">
        <img class="col-lg-5" src="./icons/PempekJumbotron.png" style="filter: drop-shadow(2px 2px 70px rgba(0, 0, 0, 0.25));">
        <div class="col-lg-7 description lh-lg  px-5" style="text-indent: 45px;">
          <p class="fs-6">
            Kami adalah sebuah usaha mikro, kecil, dan menengah (UMKM) yang berfokus pada penjualan produk pempek buatan rumah. Dengan bangga, kami menghadirkan pempek asli buatan orang Palembang, yang memiliki cita rasa autentik dan kualitas terbaik.
          </p>
          <p class="fs-6">
            Dalam lingkungan bisnis yang kompetitif saat ini, kami memahami pentingnya mempertahankan keaslian kuliner tradisional.
            Oleh karena itu, kami mengambil tanggung jawab untuk memproduksi dan menjual pempek dengan resep turun-temurun yang telah diwariskan dari generasi ke generasi.
            Setiap produk pempek yang kami tawarkan dibuat dengan cinta dan dedikasi di dalam dapur rumah kami. Kami memilih bahan-bahan berkualitas tinggi, seperti ikan segar, sagu pilihan, dan rempah-rempah alami, untuk menciptakan cita rasa yang otentik dan lezat.
          </p>
        </div>
      </div>
    </div>
    <div class="vector-tentang-kami position-absolute z-0">
        <VectorTentangKami/>
    </div>
  </div>
</template>

<style>  
  .vector-tentang-kami {
    top: 0px;
    left: 0px;
  }

  .tentangKami-content {
    justify-content: center;
  }

  .headline-2 {
  padding-top: 100px;
    font-size: 62px;
    font-weight: 700;
    text-align: center;
  }

  .line {
    margin: auto;
    width: 100px;
    height: 10px;    
    background-color:var(--primary-color);
  }
</style>