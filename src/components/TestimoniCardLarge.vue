<template>
  <div class="text-center testimonial">
    <div class="profile-photo my-4">
      <img :src="profilePhoto" class="rounded-circle">
    </div>
    <div class="username-testimonial">
      <h4 class="headline-3 fw-bold">{{ username }}</h4>
    </div>
    <hr class="m-4">
    <div class="rating-testimonial">
      <span class="rating-icon" v-for="n in rating" :key="n">&#9733;</span>
    </div>
    <div class="description-testimonial">
      <p class="mt-3 px-4">{{ description }}</p>
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
  width: 350px;
  border-radius: 10px;
  border-top: 10px solid gold;  
}

.profile-photo img {
  margin: auto;
  width: 150px;
}

.profile-photo {
  height: 140px;
}

.rating-testimonial {
  margin-top: 10px;
}

.rating-icon {
  font-size: 24px;
  color: gold;
}

@media (max-width: 768px) {}
</style>
