<script setup>
import Navbar from './components/Navbar.vue';
import Marketplace from './components/Marketplace.vue';
import TestimoniCardLarge from './components/TestimoniCardLarge.vue';
import WavesJumbotron from './components/icons/WavesJumbotron.vue';
import VectorTentangKami from './components/icons/tentang-kami.vue';
import Footer from './components/Footer.vue';
import Menu from './components/Menu.vue';
import MenuExpand from './components/MenuExpand.vue';
import Sertifikat from './components/Sertifikat.vue';


import { ref } from 'vue'

const expand = ref(false)
function toggleExpand() {
  expand.value = !expand.value
}
</script>


<template>
  <header>
    <Navbar />
  </header>

  <main>
    <section id="beranda">
      <div class="position-relative jumbotron">
        <div class="container position-relative z-1">
          <div class="row jumbotron-content">
            <div class="col-lg-7 pb-5" style="filter: drop-shadow(1px 1px 2px rgba(0, 0, 0, 0.25));">
              <h1 class="headline-1 fw-bold">Cari Makanan Tradisional <br> Palembang ?</h1>
              <p class="lead">Pempek Princess jawabannya, Asli <br> buatan orang Palembang</p>
              <a class="link" href="#menu">View Our Menu</a>
            </div>
            <div class="col-lg-5" style="filter: drop-shadow(2px 2px 10px rgba(0, 0, 0, 0.25));">
              <img class="d-block mx-auto" src="src/assets/images/PempekJumbotron.png" width="80%">
            </div>
          </div>
        </div>
        <div class="vector-jumbotron position-absolute z-0">
          <WavesJumbotron />
        </div>
      </div>
      <div class="container">
        <div class="market d-flex justify-content-evenly flex-wrap">
          <Marketplace marketplaceImage="src/assets/images/marketplace/tokopedia.png" />
          <Marketplace marketplaceImage="src/assets/images/marketplace/gofood.png"
          marketplaceLink="https://gofood.co.id/bandung/restaurant/pempek-princess-cangkuang-4bb1e789-67ba-4c7c-9445-66f1eefa239e" />
          <Marketplace marketplaceImage="src/assets/images/marketplace/shopee.png"
          marketplaceLink="https://shopee.co.id/pempekprincess" />
          <Marketplace marketplaceImage="src/assets/images/marketplace/shopee-food.png" />
        </div>
      </div>
    </section>
      
    <section id="tentang-kami">
      <div class="position-relative py-5 mt-5">
        <div class="container position-relative z-1">
          <h2 class="headline-2 pt-5">Tentang-kami</h2>
          <div class="line"></div>
          <div class="d-flex flex-wrap align-items-center justify-content-evenly tentangKami-content mt-5">
            <div class="col-lg-4">
              <img src="src/components/icons/pempek 1.png" style="filter: drop-shadow(2px 2px 70px rgba(0, 0, 0, 0.25));">
            </div>

            <div class="col-lg-8 description-tentang-kami lh-lg  px-5" style="text-indent: 45px;">
              <p class="lh-base">
                Kami adalah sebuah usaha mikro, kecil, dan menengah (UMKM) yang berfokus pada penjualan produk pempek
                buatan rumah. Dengan bangga, kami menghadirkan pempek asli buatan orang Palembang, yang memiliki cita rasa
                autentik dan kualitas terbaik.
              </p>
              <p class="lh-base">
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
          <div class="pb-5 d-flex justify-content-center">
            <Sertifikat />
          </div>
        </div>
        <div class="vector-tentang-kami position-absolute z-0">
          <VectorTentangKami />
        </div>
        <div>
        </div>
      </div>
    </section>

    <section id="menu" class="pb-5">
      <h2 class="headline-2">All Menu</h2>
      <div class="line"></div>
      <Menu />
      <div class="MenuExpand">
        <MenuExpand v-if="expand" />
      </div>
      <div class="d-flex justify-content-center">
        <button class="lihat btn mt-5 " @click="toggleExpand">
          {{ expand ? 'Tampilkan Lebih Sedikit' : 'Lihat Lebih Banyak' }}
        </button>
      </div>
    </section>

    <section class="testimoni">
      <div class="container">
        <h2 class="mt-4 mb-3 text-center headline-2">Testimoni</h2>
        <div class="line"></div>
        <div class="row mt-5 align-items-stretch justify-content-around">
          <div class="col-lg-6 p-2">
            <div class="d-flex justify-content-center">
              <TestimoniCardLarge profilePhoto="src/assets/images/profile/aldi.jpg" username="@john.doe"
                description="Maaci umi kirimannya, ini pempek kates yang bisa dikirim ke jakarta yang isinyo aman dan masih seger. mantabb"
                :rating="4" />
            </div>
          </div>
          <div class="col-lg-6 p-2">
            <div class="d-flex justify-content-center">
              <TestimoniCardLarge profilePhoto="src/assets/images/profile/aldi.jpg" username="@jane.smith"
                description="Alhamdulillah, Laksana nyo nyampe sebelum buko plus bonus talam ubi ungu, baik banget mevaah, mokaseh @pempek_princess. “maka nikmat Tuhan manalagi yg kau dusta”"
                :rating="5" />
            </div>
          </div>
          <div class="col-lg-6 p-2">
            <div class="d-flex justify-content-center">
              <TestimoniCardLarge profilePhoto="src/assets/images/profile/aldi.jpg" username="@alex.williams"
                description="Pempek Princess, lezatnya sebuah pempek tak hanya memiliki cita rasa enak dilidah saja, tetapi juga perpaduan bumbu yang menggugah selera serta membuat ketagihan."
                :rating="5" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="maps">
      <iframe width="100%" height="100%" id="gmap_canvas"
        src="https://maps.google.com/maps?q=-7.052070,107.543132&t=&z=10&ie=UTF8&iwloc=&output=embed" frameborder="0"
        scrolling="no" marginheight="0" marginwidth="0"></iframe>
    </section>

    <section id="Footer">
      <Footer />
    </section>
  </main>
</template>


<style scoped>
main {
  overflow: hidden;
}
.market {
  padding-top: 6rem;
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

.lihat {
  margin: 0 auto;
  display: block;
  width: 250px;
  text-align: center;
  padding: 5px 10px;
  background-color: var(--primary-color);
  color: white;
  text-decoration: none;
  font-size: 18px;
  font-weight: 700;
  border-radius: 20px;
  box-shadow: 0px 4px 15px 2px rgba(0, 0, 0, 0.25);
}

.line {
  margin: auto;
  width: 100px;
  height: 10px;
  background-color: var(--primary-color);
}

.link {
  padding: 10px 25px;
  background-color: var(--primary-color);
  color: white;
  text-decoration: none;
  font-weight: 700;
  border-radius: 20px;
}

.jumbotron {
  padding-top: 100px;
}

.vector-jumbotron {
  top: -50px;
  right: 0px;
}

.maps {
  margin-top: 200px;
  width: 100%;
  height: 550px;
}


@media (max-width: 992px) {
  .market {
    padding-top: 2rem;
  }
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

  .jumbotron {
    padding-top: 100px;
  }

  .vector-jumbotron {
    top: 120px;
    right: -300px;
  }

  .market {
    margin-top: 70px;
  }

  .vector-tentang-kami {
    top: 0px;
    left: -160px;
  }

  .description-tentang-kami {
    margin-top: 25px;
  }
}</style>
