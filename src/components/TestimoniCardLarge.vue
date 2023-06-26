<template>
  <div class="testimonial p-5">
    <div class="text-center">
      <div class="profile-photo">
        <img :src="profilePhoto" class="rounded-circle">
        <div class="username-testimonial pt-3">
          <h4 class="headline-3 fw-bold text-center">{{ username }}</h4>
        </div>
      </div>
      <div class="description-testimonial">
        <p class="mt-3">{{ description }}</p>
      </div>
      <div class="rating-testimonial">
        <span class="rating-icon" v-for="n in rating" :key="n">&#9733;</span>
      </div>
    </div>
  </div>
</template>



<style scoped>
.testimonial {
  margin: auto;
  width: 70%;
}

.profile-photo img {
  margin: auto;
  width: 100px;
  /* Ubah ukuran gambar sesuai kebutuhan */
}

.rating-icon {
  font-size: 24px;
  color: var(--primary-color);
}

@media (max-width: 768px) {
  .testimonial {
    width: 85%;
  }

  .description-testimonial {
    font-size: 12px;
  }

  .headline-3 {
    font-size: 16px;
  }
}
</style>


<script>
export default {
  props: {
    profilePhoto: {
      type: String,
      required: true
    },
    username: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    rating: {
      type: Number,
      required: true
    }
  }
}
</script>
