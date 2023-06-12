<template>
  <div class="card">
    <img :src="profilePhoto" alt="Profile Photo" class="card-img-top">
    <div class="card-body">
      <h5 class="card-title">{{ username }}</h5>
      <p class="card-text">{{ description }}</p>
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
    }
  }
}
</script>

<style scoped>
.card {
  width: 18rem;
  margin-bottom: 1.5rem;
}
</style>
