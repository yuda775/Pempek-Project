<template>
  <div class="marketplace d-flex justify-content-center align-items-center m-2">
    <a :href="marketplaceLink">
      <img :src="`../assets/images/marketplace/${marketplaceImage}`">
    </a>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  marketplaceImage: String,
  marketplaceLink: String
});
</script>

<style>
.marketplace {
  width: 5rem;
  height: 5rem;
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
    width: 4rem;
    height: 4rem;
  }
}
</style>