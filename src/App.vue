<script setup>
import Marketplace from './components/Marketplace.vue';
import TestimoniCardLarge from './components/TestimoniCardLarge.vue';
import WavesJumbotron from './components/icons/WavesJumbotron.vue';
import VectorTentangKami from './components/icons/tentang-kami.vue';
import Footer from './components/Footer.vue';
import Menu from './components/Menu.vue';
import MenuExpand from './components/MenuExpand.vue';
import Sertifikat from './components/Sertifikat.vue';
import Menus from './components/Menus.vue';


import { ref, onMounted, onUnmounted } from 'vue';


// ==== Popup Sertifikat =====
const expand = ref(false)
function toggleExpand() {
  expand.value = !expand.value
}


// ==== Navbar ====
const activeSection = ref('beranda');
const isScrolled = ref(false);

const setActiveSection = (section) => {
  activeSection.value = section;
};

const handleScroll = () => {
  isScrolled.value = window.scrollY > 0;
  const scrollPosition = window.scrollY;
  // Cek posisi scroll dan perbarui item navbar yang aktif
  if (scrollPosition >= 0 && scrollPosition < 500) {
    activeSection.value = 'beranda';
  } else if (scrollPosition >= 500 && scrollPosition < 1000) {
    activeSection.value = 'tentang-kami';
  } else if (scrollPosition >= 1000) {
    activeSection.value = 'menu';
  }
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

// Membersihkan event listener saat komponen di-unmount
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});


</script>


<template>
  <header>
    <nav class="navbar navbar-expand-lg fixed-top" :class="{ 'scrolled': isScrolled }">
      <div class="container">
        <a class="navbar-brand" href="#"><img src="/assets/brand-logo.png" alt="brand-logo" width="125" /></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav mx-auto">
            <a class="nav-link" :class="{ 'active': activeSection === 'beranda' }" @click="setActiveSection('beranda')"
              href="#beranda">Beranda</a>
            <a class="nav-link" :class="{ 'active': activeSection === 'tentang-kami' }"
              @click="setActiveSection('tentang-kami')" href="#tentang-kami">Tentang Kami</a>
            <a class="nav-link" :class="{ 'active': activeSection === 'menu' }" @click="setActiveSection('menu')"
              href="#menu">Menu</a>
          </div>
          <div class="button" :class="{ 'scrolled': isScrolled }">
            <a class="fw-bold" href="https://api.whatsapp.com/message/23Z4KIC2KKJXA1?autoload=1&app_absent=0">Kontak</a>
          </div>
        </div>
      </div>
    </nav>
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
              <img class="d-block mx-auto" src="/assets/pempek-hero.png" width="">
            </div>
          </div>
        </div>
        <div class="vector-jumbotron position-absolute z-0">
          <WavesJumbotron />
        </div>
      </div>
      <div class="container">
        <div class="market d-flex justify-content-center gap-5 flex-wrap">
          <Marketplace marketplaceImage="/assets/marketplace/gofood.png"
            marketplaceLink="https://gofood.co.id/bandung/restaurant/pempek-princess-cangkuang-4bb1e789-67ba-4c7c-9445-66f1eefa239e" />
          <Marketplace marketplaceImage="/assets/marketplace/shopee.png"
            marketplaceLink="https://shopee.co.id/pempekprincess" />
          <Marketplace marketplaceImage="/assets/marketplace/shopee-food.png" />
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
              <img src="/assets/about.png" style="filter: drop-shadow(2px 2px 70px rgba(0, 0, 0, 0.25));">
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
        <div>
        </div>
        <div class="vector-tentang-kami position-absolute z-0">
          <VectorTentangKami />
        </div>
      </div>
    </section>

    <!-- <section id="menu" class="pb-5">
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
    </section> -->

    <section id="menu">
      <h2 class="headline-2">All Menu</h2>
      <div class="line"></div>
      <menus />
    </section>

    <section class="maps">
      <iframe width="100%" height="100%" id="gmap_canvas"
        src="https://maps.google.com/maps?q=-7.052070,107.543132&t=&z=10&ie=UTF8&iwloc=&output=embed" frameborder="0"
        scrolling="no" marginheight="0" marginwidth="0"></iframe>
    </section>

    <section class="testimoni">
      <h2 class="mt-4 mb-3 text-center headline-2">Testimoni</h2>
      <div class="line"></div>
      <div class="container">
        <div id="carouselExampleRide" class="carousel slide" data-bs-ride="true">
          <div class="carousel-inner">
            <div class="carousel-item active">
              <TestimoniCardLarge profilePhoto="/assets/profile/testi1.jpg" username="@bundaaratu_"
                description="Maaci umi kirimannya, ini pempek kates yang bisa dikirim ke jakarta yang isinyo aman dan masih seger. mantabb"
                :rating="4" />
            </div>
            <div class="carousel-item">
              <TestimoniCardLarge profilePhoto="/assets/profile/testi2.jpg" username="@iranurfaz_"
                description="Alhamdulillah, Laksana nyo nyampe sebelum buko plus bonus talam ubi ungu, baik banget mevaah, mokaseh @pempek_princess. “maka nikmat Tuhan manalagi yg kau dusta”"
                :rating="5" />
            </div>
            <div class="carousel-item">
              <TestimoniCardLarge profilePhoto="/assets/profile/testi3.jpg" username="@widya_rose"
                description="Pempek Princess, lezatnya sebuah pempek tak hanya memiliki cita rasa enak dilidah saja, tetapi juga perpaduan bumbu yang menggugah selera serta membuat ketagihan."
                :rating="5" />
            </div>
          </div>
          <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleRide" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleRide" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
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

.carousel-control-prev-icon,
.carousel-control-next-icon {
  filter: invert(100%);
}


/* Navbar */
.navbar {
  font-family: var(--primary-font-family);
}

.nav-link {
  text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
  min-width: 125px;
  text-align: center;
  font-weight: 600;
}

.button a {
  font-size: 18px;
  color: var(--primary-color);
  background-color: #FFFFFF;
  padding: 5px 30px;
  border-radius: 2px;
  text-decoration: none;
  transition: background-color 0.8s;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
  border-radius: 100px;
}

.nav-link:hover {
  color: var(--primary-color);
  font-weight: bold;
}

.button a:hover {
  color: white;
  background-color: transparent;
  border: 2px solid white;
  padding: 3px 28px;
  /* Ubah padding sesuai dengan ukuran awal */
}


/* Gaya untuk navbar dengan background putih saat scroll */
.scrolled {
  background-color: #FFFFFF;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
}

/* Gaya untuk navbar-link yang sedang aktif (kuning) */
.navbar .nav-link.active {
  color: var(--primary-color);
  border-bottom: 2px solid var(--primary-color);
}

/* Gaya untuk navbar-link saat dihover (bold) */
.navbar .nav-link:hover {
  font-weight: bold;
}

.button.scrolled a {
  color: #FFFFFF;
  background-color: var(--primary-color);
  /* Ubah warna background sesuai kebutuhan */
}

.scrolled .button a:hover {
  color: var(--primary-color);
  background-color: transparent;
  border: 2px solid var(--primary-color);
  padding: 2px 28px;
  /* Ubah padding sesuai dengan ukuran awal */
}

/* Akhir Navbar */

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

  .navbar,
  .collapse .navbar-collapse {
    background-color: #FFFFFF;
  }

  .navbar-nav {
    flex-direction: column;
    align-items: center;
  }

  .navbar-brand {
    width: 100px;
  }

  .navbar-nav .nav-link {
    margin: 0.5rem 0;
  }

  .button {
    text-align: center;
    margin: 2rem;
  }

  .button a {
    color: #FFFFFF;
    background-color: var(--primary-color);
  }

  .button a:hover {
    color: var(--primary-color);
    background-color: transparent;
    border: 2px solid var(--primary-color);
  }

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
    margin-top: 14px;
  }
}
</style>
