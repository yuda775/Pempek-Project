<template>
  <div>
    <button @click="openModal" class="btn tombol-halal">Lihat Sertifikat Halal</button>

    <div class="modal" :class="{ 'd-block': showModal }">
      <div class="modal-dialog modal-dialog-centered modal-sm ">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title fs-6 fw-bold">Sertifikat Halal LPOM MUI</h5>
            <button @click="closeModal" type="button" class="close text-dark fs-4" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <img src="../../public/images/sertifikat.jpeg" class="img-fluid" alt="Gambar Modal">
          </div>
          <div class="moda-footer">
            <p class="px-3">Untuk Informasi lebih lengkap klik link <a href="">disini</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    }
  }
};
</script>


<style scoped>
.modal {
  margin-top: 2rem;
}

.modal-header {
  padding: 0.5px 1rem;
}

.tombol-halal {
  background-color: var(--primary-color);
  color: white;
}

.tombol-halal:hover {
  background-color: #f5f5f5;
  color: var(--primary-color);
  font-weight: bold;
}

.modal-dialog {
  min-width: 25vw;
}</style>