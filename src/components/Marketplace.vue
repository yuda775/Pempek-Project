<template>
  <div class="d-flex justify-content-evenly mt-5">
    <div class="marketplace col-md-4">
      <img src="./icons/tokopedia.png" >
    </div>
    <div class="marketplace col-md-4">
      <img src="./icons/shopee-food.png" >
    </div>
    <div class="marketplace col-md-4">
      <img src="./icons/gofood.png" >
    </div>
  </div>
</template>

<style>
.marketplace {
  display: flex;
  justify-content: center; /* Mengatur posisi horizontal gambar di tengah */
  align-items: center; /* Mengatur posisi vertikal gambar di tengah */
  width: 150px;
  height: 150px;
  background-color: white;
  padding: 20px;
  border-radius: 50%;
  filter: drop-shadow(0px 0px 25px rgba(0, 0, 0, 0.25));
}
</style>