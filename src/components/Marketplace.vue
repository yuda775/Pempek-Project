<template>
  <div class="marketplace d-flex justify-content-center align-items-center m-2">
    <a :href="marketplaceLink">
      <img :src="marketplaceImage">
    </a>
  </div>
</template>


<style>
.marketplace {
  width: 100px;
  height: 100px;
  background-color: white;
  padding: 13px;
  border-radius: 50%;
  filter: drop-shadow(0px 0px 5px rgba(0, 0, 0, 0.25));
}

.marketplace:hover {
  filter: drop-shadow(0px 0px 10px rgb(255, 139, 14));
  transition: 1s;
}


@media (max-width: 992px){
  .marketplace {
    width: 80px;
    height: 80px;
  }
}
</style>

<script setup>
  const props = defineProps({
    marketplaceImage: String,
    marketplaceLink: String
  })
</script>
