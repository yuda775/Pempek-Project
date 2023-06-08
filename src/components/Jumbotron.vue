<template>
  <div class="jumbotron">
    <div class="container">
      <div class="content">
        <h1>Cari Makanan Tradisional <br> Palembang ?</h1>
        <p>
          Pempek Princess Jawabannya, Asli <br>
          buatan orang Palembang.
        </p>
        <a class="link" href="#menu">View Our Menu</a>         
      </div>
      <figure>
        <img class="enlarged-image" src="./icons/pempek Jumbotron.svg" alt="gambar pempek">
      </figure>          
    </div>
  </div>
</template>

<style>

.jumbotron {
  aspect-ratio: 16/9;
  background-image: url(./icons/Vector.svg);
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
}

.content {
  flex: 1;
  padding-right: 20px;
  padding-top: 200px;
}

h1 {
  padding: 1px 20px;
  border-left: 10px solid var(--primary-color);
  font-weight: 700;
  color: var(--secondary-color);
  font-size: 3.2vw;
}

p {
  margin-top: 30px;
  font-size: 24px;
  margin-bottom: 30px;
}

.link {  
  background-color: var(--primary-color);
  padding: 10px 25px;font-weight: 700;
  color: white;
  text-decoration: none;
  font-weight: 18px;
  background: #FF9F0D;
  border-radius: 20px;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}


.enlarged-image {
  position: absolute;
  width: 60vw;
  top: 120px;
  right: 10px;
  filter: drop-shadow(28px 44px 90px rgba(0, 0, 0, 0.25));
}

</style>
