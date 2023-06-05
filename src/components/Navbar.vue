<template>
  <nav class="navbar navbar-expand-lg fixed-top" :class="{ 'scrolled': isNavbarScrolled }">
    <div class="container-fluid">
      <a class="navbar-brand" href="#"><img src="./icons/pempek.png" alt="brand-logo" width="125"></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav mx-auto fw-semibold">
          <a class="nav-link" :class="{ 'active': activeSection === 'beranda' }" href="#beranda">Beranda</a>
          <a class="nav-link" :class="{ 'active': activeSection === 'menu' }" href="#menu">Menu</a>
          <a class="nav-link" :class="{ 'active': activeSection === 'tentang-kami' }" href="#tentang-kami">Tentang Kami</a>
        </div>
        <div class="button">
          <a class="fw-bold" href="#kontak">Kontak</a>       
        </div>
      </div>
    </div>
  </nav>  
</template>

<style>
a {
  font-family: var(--tertiary-font-family);
  text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
}

.button a {
  font-size: 18px;
  width: 110px;
  color: var(--primary-color);
  background-color: #FFFFFF;
  padding: 8px 20px;
  border-radius: 2px;
  text-decoration: none;
  transition: background-color 0.8s;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
}

.nav-link:hover {
  color: var(--primary-color);
}

.button a:hover {
  background-color: transparent;
  border: 3px solid #FFFFFF;
  color: #FFFFFF;
  padding: 5px 17px;
}

.navbar.scrolled {
  background-color: #FFFFFF;
}

.navbar.scrolled a {
  color: var(--primary-color);
}

.navbar.scrolled a:hover {
  font-weight: bold;
  color: var(--secondary-color);
}

.navbar.scrolled .button a {
  background-color: var(--primary-color);
  color: #FFFFFF;
}

.navbar.scrolled .button a:hover {
  background-color: transparent;
  color: var(--primary-color);
  border: 3px solid var(--primary-color);
}

.nav-link.active {
  color: var(--secondary-color);
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

  .navbar-toggler {
    margin-bottom: 1rem;
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
</style>


<script>
  export default {
    data() {
      return {
        isNavbarScrolled: false,
        activeSection: 'beranda'
      };
    },
    mounted() {
      if (window.innerWidth > 992) {
        window.addEventListener('scroll', this.handleScroll);
      }
    },
    beforeDestroy() {
      if (window.innerWidth > 992) {
        window.removeEventListener('scroll', this.handleScroll);
      }
    },
    methods: {
      handleScroll() {
        this.isNavbarScrolled = window.scrollY > 0;

        const sections = ['beranda', 'menu', 'tentang-kami'];
        const scrollTop = window.scrollY;
        const windowHeight = window.innerHeight;
        const sectionOffsets = sections.map(section => ({
          id: section,
          offset: document.getElementById(section).offsetTop
        }));

        const activeSection = sectionOffsets.find(section => scrollTop >= section.offset && scrollTop < section.offset + windowHeight);

        if (activeSection) {
          this.activeSection = activeSection.id;
        }
      }      
    }
  };
</script>