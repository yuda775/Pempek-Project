<template>
  <div class="overflow-x-hidden mt-3">
    <div class="row justify-content-evenly p-5">
      <div class="marketplace col-lg-4">
        <a href="">
          <img src="./icons/tokopedia.png" >
        </a>
      </div>
      <div class="marketplace col-lg-4">
        <a href="">
          <img src="./icons/shopee-food.png" >
        </a>
      </div>
      <div class="marketplace col-lg-4">
        <a href="">
          <img src="./icons/gofood.png" >
        </a>
      </div>
    </div>
  </div>
</template>

<style>
.marketplace {
  display: flex;
  justify-content: center; /* Mengatur posisi horizontal gambar di tengah */
  align-items: center; /* Mengatur posisi vertikal gambar di tengah */
  width: 125px;
  height: 125px;
  background-color: white;
  padding: 20px;
  border-radius: 50%;
  filter: drop-shadow(0px 0px 5px rgba(0, 0, 0, 0.25));
}

.marketplace:hover {
  filter: drop-shadow(0px 0px 25px rgb(255, 139, 14));
  transition: 1s;
}
</style>