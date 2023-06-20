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

<script>
export default {
  data() {
    return {
      expanded: false,

      cards: [
        {
          id: 1,
          title: 'Pempek Kapal Selam',
          description: 'Memliki bentuk seperti  kapal selam,  pempek ini berisikan telor didalam. pempek ini bisa disajikan dengan timun ',
          image: 'src/assets/images/kapalselam.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 2,
          title: 'Pempek Adaan',
          description: 'Berbentuk bulat seperti bola ping pong. Pempek ini terbuat juga dari ikan, sehingga sekilas memang seperti bakso ikan.',
          image: 'src/assets/images/adaan.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 3,
          title: 'Pempek Kulit',
          description: 'Pempek kulit biasanya menggunakan campuran tepung dan adonan kulit ikan. Ikan yang paling sering digunakan adalah ikan tenggiri.',
          image: 'src/assets/images/kulit.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 4,
          title: 'Pempek Keriting',
          description: 'Pempek keriting umumnya hanya ditemukan di wilayah Palembang. dikarenakan proses pembuatannya yang rumit dan membutuhkan waktu yang lama.',
          image: 'src/assets/images/keriting.png',
          price: 'Rp.15.000 / porsi'
        },
      ]
    };
  }
};
</script>

