<script setup>
import Navbar from './components/Navbar.vue';
import Marketplace from './components/Marketplace.vue';
import Menu from './components/Menu.vue';
import TestimoniCard from './components/TestimoniCard.vue';
import TestimoniCardLarge from './components/TestimoniCardLarge.vue';
import WavesJumbotron from './components/icons/WavesJumbotron.vue';
import VectorTentangKami from './components/icons/tentang-kami.vue';
import vectorleft from './components/icons/vectorleft.vue';
import vectorright from './components/icons/vectorright.vue';
</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>

    <section id="beranda">
      <div class="position-relative overflow-x-hidden">
        <div class="container">
          <div class="jumbotron row align-items-center z-2">
            <div class="title col-lg-6">
              <h1 class="headline-1">Cari Makanan Tradisional <br> Palembang ?</h1>
              <p class="lead">Pempek Princess jawabannya, Asli <br> buatan orang Palembang</p>
              <a class="link" href="#menu">View Our Menu</a>
            </div>
            <div class="col-lg-6 mt-5" style="filter: drop-shadow(2px 2px 70px rgba(0, 0, 0, 0.25));">
              <img src="src/assets/images/PempekJumbotron.png" alt="">
            </div>
          </div>
        </div>
        <div class="vector-jumbotron">
          <WavesJumbotron />
        </div>
      </div>
    </section>

    <Marketplace />
    <section id="tentang-kami">
      <div class="position-relative">
        <div class="container position-relative z-1">
          <h2 class="headline-2">Tentang-kami</h2>
          <div class="line"></div>
          <div class="row align-items-center tentangKami-content mt-5">
            <img class="col-lg-5 tentang-kami-img" src="src/assets/images/PempekJumbotron.png"
              style="filter: drop-shadow(2px 2px 70px rgba(0, 0, 0, 0.25));">
            <div class="col-lg-7 description-tentang-kami lh-lg  px-5" style="text-indent: 45px;">
              <p class="fs-6">
                Kami adalah sebuah usaha mikro, kecil, dan menengah (UMKM) yang berfokus pada penjualan produk pempek
                buatan rumah. Dengan bangga, kami menghadirkan pempek asli buatan orang Palembang, yang memiliki cita rasa
                autentik dan kualitas terbaik.
              </p>
              <p class="fs-6">
                Dalam lingkungan bisnis yang kompetitif saat ini, kami memahami pentingnya mempertahankan keaslian kuliner
                tradisional.
                Oleh karena itu, kami mengambil tanggung jawab untuk memproduksi dan menjual pempek dengan resep
                turun-temurun yang telah diwariskan dari generasi ke generasi.
                Setiap produk pempek yang kami tawarkan dibuat dengan cinta dan dedikasi di dalam dapur rumah kami. Kami
                memilih bahan-bahan berkualitas tinggi, seperti ikan segar, sagu pilihan, dan rempah-rempah alami, untuk
                menciptakan cita rasa yang otentik dan lezat.
              </p>
            </div>
          </div>
        </div>
        <div class="vector-tentang-kami position-absolute z-0">
          <VectorTentangKami />
        </div>
      </div>
    </section>

    <section id="menu">
      <Menu />
    </section>
    <section id="testimoni">
      <div class="container">
        <h2 class="mt-4 mb-3 text-center headline-2">Testimoni</h2>
        <div class="line"></div>
        <div class="vectortestimoni">
          <div class="vector-left">
            <vectorleft />
          </div>
          <div class="vector-right">
            <vectorright />
          </div>
        </div>
        <div class="cards row mt-5 align-items-center">
          <div class="col-md-4">
            <div class="d-flex justify-content-center px-5">
              <TestimoniCard profilePhoto="src/assets/images/profile/aldi.jpg" username="@john.doe"
                description="Maaci umi kirimannya, ini pempek kates yang bisa dikirim ke jakarta yang isinyo aman dan masih seger. mantabb" />
            </div>
          </div>
          <div class="col-md-4">
            <div class="d-flex justify-content-center">
              <TestimoniCardLarge profilePhoto="src/assets/images/profile/aldi.jpg" username="@jane.smith"
                description="Alhamdulillah, Laksana nyo nyampe sebelum buko plus bonus talam ubi ungu, baik banget mevaah, mokaseh @pempek_princess. “maka nikmat Tuhan manalagi yg kau dusta”" />
            </div>
          </div>
          <div class="col-md-4">
            <div class="d-flex justify-content-center px-5">
              <TestimoniCard profilePhoto="src/assets/images/profile/aldi.jpg" username="@alex.williams"
                description="Pempek Princess, lezatnya sebuah pempek tak hanya memiliki cita rasa enak dilidah saja, tetapi juga perpaduan bumbu yang menggugah selera serta membuat ketagihan." />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section>
      <div class="maps">
        <iframe width="100%" height="100%" id="gmap_canvas" src="https://maps.google.com/maps?q=-7.052070,107.543132&t=&z=10&ie=UTF8&iwloc=&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe>
      </div>
    </section>
  </main>
</template>

<style scoped>
main {
  height: 20000px;
}

.vector-tentang-kami {
  top: 0px;
  left: 0px;
}

.tentangKami-content {
  justify-content: center;
}

.headline-1 {
  font-size: 42px;
  font-weight: 700;
  color: var(--secondary-color);
  border-left: 10px solid var(--primary-color);
  padding-left: 10px;
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
  background-color: var(--primary-color);
}

.jumbotron {
  position: relative;
  padding-top: 100px;
  padding-bottom: 200px;
  justify-content: space-evenly;
  z-index: 1;
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

.vector-left {
  position: absolute;
  top: 3690px;
  left: 400px;
}

.vector-right {
  position: absolute;
  top: 3920px;
  right: 400px;
}

.maps{
  margin-top: 200px;
  width: 100%;
  height: 550px;
}


@media (max-width: 767.98px) {
  .headline-1 {
    font-size: 32px;
    border-left: 5px solid var(--primary-color);
  }

  .headline-2 {
    font-size: 28px;
  }

  .line {
    height: 5px;
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

  .vector-tentang-kami {
    top: 0px;
    left: -180px;
  }

  .tentang-kami-img {
    width: 80%;
  }

  .description-tentang-kami {
    margin-top: 25px;
  }
}</style>