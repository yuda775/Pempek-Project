<template>
  <div class="card card-testimoni p-3">
    <div class="card-body d-flex flex-column justify-content-around">
      <img :src="profilePhoto" alt="Profile Photo" class="card-img-top rounded-circle">
      <div class="py-4">
        <h5 class="card-title text-center p-2">{{ username }}</h5>
        <p class="card-text px-3 py-2">{{ description }}</p>
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
    }
  }
}


</script>

<style scoped>

.card-testimoni {
  height: 400px;
}
.card-img-top {
  margin: 0 auto;  
  width: 100px;
  height: 100px;
}
.card-title {
  font-size: 22px;
  font-weight: 600;
}
.card-text {  
  font-size: 14px;
  border-left: 5px solid var(--primary-color);
}
</style>