<template>
  <div class="jumbotron">
    <div class="jumbotron-text">
      <div class="jumbotron-heading">      
        <h1>Pempek</h1>
        <span>Princess</span>
      </div>
      <p>Asli Buatan Orang Palembang</p>
    </div>
    <div class="jumbotron-image">
      <img src="./icons/pempek-jumbotron.png" alt="Gambar" width="850">
    </div>
  </div>
</template>


<style>
  .jumbotron {
    background-image: url(./icons/jumbotron-background.svg);
    background-repeat: no-repeat;
    background-size: cover;
    aspect-ratio: 16/9;
    display: flex;
    padding-top: 150px;
    justify-content: center;
  }

  .jumbotron-heading {
    position: relative;
    text-shadow: 2px 4px 5px rgba(0, 0, 0, 0.25);
  }

  .jumbotron-heading span {
    position: absolute;    
    font-family: var(--secondary-font-family);
    margin-top: -65px;
    margin-left: 300px;
    font-weight: bold;
    font-size: 42px;
    font-style: italic;
    text-shadow: 2px 4px 5px rgba(0, 0, 0, 0.25);
  }

  p {
    font-family: var(--tertiary-font-family);
    font-style: italic;
    font-weight: 400;
    font-size: 18px;
    line-height: 22px;

    color: #2C2C2C;
  }

  h1 {
    font-family: var(--primary-font-family);
    font-size: 180px;    
    color: var(--primary-color);
  }


  @media (max-width: 992px) {
    .jumbotron {
      margin-top: 85px;
      background-image: url(./icons/jumbotron-mobile.svg);
      aspect-ratio: 9/16;
    }
  }
</style>