<template>
  <div class="container">
    <div class="row">
      <div class="d-flex flex-wrap justify-content-evenly align-items-center flex-wrap mb-2">
        <div class="col-lg-3 col-md-4 col-sm-4 mt-5" v-for="card in cards" :key="card.id">
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

   
<style>
.card-text {
  font-size: 13px;
}

.card-body {
  height: 9rem;
}

.card-menu {
  box-shadow: 0px 4px 10px rgba(128, 109, 97, 0.5);
  border-radius: 20px 5px 0px 0px;
  width: 240px;
  margin: auto;
}


.price {
  border-radius: 0px 20px 0px 0px;
  font-size: 13px;
  color: white;
  font-weight: bold;
  padding: 13px 30px;
  display: inline;
  background-color: var(--primary-color);
  margin-bottom: 100px;
}

/* Media query untuk ukuran layar di bawah laptop atau desktop */
@media screen and (max-width: 1199px) {
  .card-menu {
    width: 180px;
    /* Mengurangi lebar card-menu */
  }

  .card-title {
    font-size: 12px;
    /* Mengurangi ukuran font card-title */
  }

  .card-text {
    font-size: 9px;
    /* Mengurangi ukuran font card-text */
  }

  .price {
    font-size: 12px;
    /* Mengurangi ukuran font price */
  }
}

@media screen and (max-width: 991px) {
  .card-menu {
    width: 150px;
    /* Mengurangi lebar card-menu lebih lanjut */
  }

  .card-title {
    font-size: 10px;
    /* Mengurangi ukuran font card-title lebih lanjut */
  }

  .card-text {
    font-size: 9px;
    /* Mengurangi ukuran font card-text lebih lanjut */
  }

  .price {
    font-size: 10px;
    /* Mengurangi ukuran font price lebih lanjut */
  }
}
</style>
 

<script>
export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          title: 'Pempek Kapal Selam',
          description: 'Memliki bentuk seperti  kapal selam,  pempek ini berisikan telor didalam. pempek ini bisa disajikan dengan timun ',
          image: '../public/images/kapalselam.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 2,
          title: 'Pempek Adaan',
          description: 'Berbentuk bulat seperti bola ping pong. Pempek ini terbuat juga dari ikan, sehingga sekilas memang seperti bakso ikan.',
          image: '../public/images/adaan.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 3,
          title: 'Pempek Kulit',
          description: 'Pempek kulit biasanya menggunakan campuran tepung dan adonan kulit ikan. Ikan yang paling sering digunakan adalah ikan tenggiri.',
          image: '../public/images/kulit.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 4,
          title: 'Pempek Keriting',
          description: 'Pempek keriting umumnya hanya ditemukan di wilayah Palembang. dikarenakan proses pembuatannya yang rumit dan membutuhkan waktu yang lama.',
          image: '../public/images/keriting.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 5,
          title: 'Pempek Tunu',
          description: 'Pempek tunu mirip seperti pempek lenggang karena biasanya diolah dengan dibakar atau dipanggang.',
          image: '../public/images/panggang.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 6,
          title: 'Pempek Pistel Dos',
          description: 'Adonan yang sama dengan lenjer namun dibentuk seperti pastel dan memiliki isan pepaya muda.',
          image: '../public/images/pempekdos.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 7,
          title: 'Pempek Otak-otak',
          description: 'Pempek Otak-otak yang dibungkus dengan daun pisang, memiliki bentuk lonjong dapat dipadukan dengan cuko merah.',
          image: '../public/images/otakotak.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 8,
          title: 'Pempek Tekwan',
          description: 'Tekwan merupakan varian dari pempek, berbahan dasar dari sagu dan ikan tersebut. Biasanya diberi tambahan jamur kuping',
          image: '../public/images/tekwan.png',
          price: 'Rp.15.000 / porsi'
        },

      ]
    };
  }
};
</script>