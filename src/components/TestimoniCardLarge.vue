<template>
  <div class="testimonial">
    <div class="d-flex align-items-stretch justify-content-around">
      <div class="col-4">
        <div class="profile-photo">
          <img :src="profilePhoto" class="rounded-circle">
          <div class="username-testimonial pt-3">
            <h4 class="headline-3 fw-bold text-center">{{ username }}</h4>
          </div>
        </div>
      </div>
      <div class="col-7">
        <div class="description-testimonial">
          <p class="mt-3">{{ description }}</p>
        </div>
        <div class="rating-testimonial">
          <span class="rating-icon" v-for="n in rating" :key="n">&#9733;</span>
        </div>
      </div>
    </div>
  </div>
</template>


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

<style scoped>
.testimonial {
  padding: 10px;
  border-radius: 10px;
  border: 2px solid var(--secondary-color);
}

.profile-photo img {
  margin: auto;
  width: 150px;
  /* Ubah ukuran gambar sesuai kebutuhan */
}

.rating-icon {
  font-size: 24px;
  color: var(--primary-color);
}

@media (max-width: 768px) {
  .description-testimonial {
    font-size: 12px;
  }
  .headline-3 {
    font-size: 16px;
  }
}
</style>
