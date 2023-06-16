<template>
    <div class="container">
      <div class="row">
        <div class="d-flex justify-content-around align-items-center flex-wrap mb-5">
          <div class="col-lg-4 mt-5" v-for="card in cards" :key="card.id">
            <div class="card-menu">
              <img :src="card.image" class="card-img-top" alt="Card Image">
              <div class="card-body mt-5">
                <h3 class="card-title px-4 fs-2">{{ card.title }}</h3>
                <p class="card-text px-4 mt-5 fs-5">{{ card.description }}</p>
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
.headline-2 {
  padding-top: 100px;
  font-size: 62px;
  font-weight: 700;
  text-align: center;
}

.card-body {
  height: 265px;
}

.card-menu {
  box-shadow: 0px 4px 10px rgba(128, 109, 97, 0.5);
  border-radius: 30px 10px 0px 0px;
  width: 400px;
}


.price {
  border-radius: 0px 20px 0px 0px;
  font-size: 20px;
  color: white;
  font-weight: bold;
  padding: 10px 40px;
  display: inline;
  background-color: var(--primary-color);
  margin-bottom: 100px;
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
        {
          id: 5,
          title: 'Pempek Tunu',
          description: 'Pempek tunu mirip seperti pempek lenggang karena biasanya diolah dengan dibakar atau dipanggang.',
          image: 'src/assets/images/panggang.png',
          price: 'Rp.15.000 / porsi'
        },
        {
          id: 6,
          title: 'Pempek Pistel Dos',
          description: 'Adonan yang sama dengan lenjer namun dibentuk seperti pastel dan memiliki isan pepaya muda.',
          image: 'src/assets/images/pempekdos.png',
          price: 'Rp.15.000 / porsi'
        }
      ]
    };
  }
};
</script>