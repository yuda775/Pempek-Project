<template>
  <nav class="navbar navbar-expand-lg fixed-top" :class="{ 'scrolled': isScrolled }">
    <div class="container">
      <a class="navbar-brand" href="#"><img src="./icons/pempek.png" alt="brand-logo" width="125"></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav mx-auto">
          <a class="nav-link" :class="{ 'active': activeSection === 'beranda' }" :href="'#beranda'">Beranda</a>
          <a class="nav-link" :class="{ 'active': activeSection === 'menu' }" :href="'#menu'">Menu</a>
          <a class="nav-link" :class="{ 'active': activeSection === 'tentang-kami' }" :href="'#tentang-kami'">Tentang Kami</a>
        </div>
        <div class="button">
          <a class="fw-bold" :href="'#kontak'">Kontak</a>
        </div>
      </div>
    </div>
  </nav>
</template>


<script>
export default {
  data() {
    return {
      isScrolled: false,
      activeSection: ''
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
    this.setActiveSection();
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.pageYOffset > 0;
      this.setActiveSection();
    },
    setActiveSection() {
      const sections = ['beranda', 'menu', 'tentang-kami'];
      const scrollPosition = window.pageYOffset + window.innerHeight / 2;
      const activeSectionIndex = sections.findIndex(section => {
        const element = document.getElementById(section);
        if (element) {
          const rect = element.getBoundingClientRect();
          return rect.top <= scrollPosition && rect.bottom >= scrollPosition;
        }
        return false;
      });
      this.activeSection = sections[activeSectionIndex] || '';
    }
  }
};
</script>

<style>
.navbar {
  font-family: var(--primary-font-family);  
}

.nav-link {
  text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
  min-width: 125px;
  text-align: center;
  font-weight: 600;
}

.button a {
  font-size: 18px;
  color: var(--primary-color);
  background-color: #FFFFFF;
  padding: 8px 30px;
  border-radius: 2px;
  text-decoration: none;
  transition: background-color 0.8s;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
  border-radius: 100px;
}

.nav-link:hover {
  color: var(--primary-color);
  font-weight: bold;
}

.button a:hover {
  color: var(--primary-color);
  background-color: transparent;
  border: 3px solid var(--primary-color);
  padding: 8px 28px;
}

/* Perubahan untuk tampilan mobile */
@media (max-width: 992px) {
  .navbar {
    background-color: #FFFFFF;
  }

  .navbar-nav {
    flex-direction: column;
    align-items: center;
  }

  .navbar-nav .nav-link {
    margin: 0.5rem 0;
  }

  .button {
    text-align: center;
    margin: 2rem;
  }

  .button a {
    color: #FFFFFF;
    background-color: var(--primary-color);
  }

  .button a:hover {
    color: var(--primary-color);
    background-color: transparent;
    border: 3px solid var(--primary-color);
  }
}

/* Gaya untuk navbar dengan background putih saat scroll */
.scrolled {
  background-color: #FFFFFF;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
}

/* Gaya untuk navbar-link yang sedang aktif (kuning) */
.navbar .nav-link.active {
  color: var(--primary-color);
  border-bottom: 2px solid var(--primary-color);
}

/* Gaya untuk navbar-link saat dihover (bold) */
.navbar .nav-link:hover {
  font-weight: bold;
}
</style>
