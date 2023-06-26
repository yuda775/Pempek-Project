
<template>
    <div class="footer-content text-center position-relative">
        <div class=" position-relative z-1">
            <div class="logo-container">
                <img class="logo d-block mx-auto" src="/assets/brand-logo.png" alt="brand-logo" width="125">
            </div>
            <div class="address d-flex justify-content-center ">
                <p class="fw-bold w-75">Jl. Cangkuang, Nagrak, Kec. Cangkuang, Kabupaten Bandung, Jawa Barat 40238</p>
            </div>
            <div class="social-icons">
                <a class="icon" href="#"><font-awesome-icon class="font-awesome" :icon="['fab', 'facebook']" /></a>
                <a class="icon" href="#"><font-awesome-icon class="font-awesome" :icon="['fab', 'twitter']" /></a>
                <a class="icon" href="#"><font-awesome-icon class="font-awesome" :icon="['fab', 'instagram']" /></a>
            </div>
            <div class="copyright pb-5">
                <p>&copy; 2023 All rights reserved by Nash<span class="kuning"> Tech</span></p>
            </div>
        </div>
        <div class="vector-footer position-absolute z-0">
            <Vectorfooter />
        </div>
    </div>
</template>
  
<style scoped>
.vector-footer {
    bottom: 0px;
    right: 0;
}

.font-awesome {
    width: min-content;
}

.social-icons {
    display: flex;
    justify-content: center;
    gap: 15px;
}

.footer-content {
    margin-top: 200px;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    align-items: center;
    text-align: center;
}

.address {
    font-weight: bold;
    font-style: italic;
}

.icon {
    font-size: 25px;
    border-radius: 100%;
    color: var(--secondary-color);
    transition: color 0.3s ease;
}

.icon:hover {
    color: var(--primary-color);
}

.kuning {
    color: var(--primary-color);
}

@media (max-width: 991.98px) {
    .vector-footer {
        bottom: -70px;
        right: -40px
    }
}
</style>
  

<script >
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { library } from '@fortawesome/fontawesome-svg-core'
import { faFacebook, faTwitter, faInstagram } from '@fortawesome/free-brands-svg-icons'
import Vectorfooter from './icons/vectorfooter.vue';

library.add(faFacebook, faTwitter, faInstagram)

export default {
    components: {
        FontAwesomeIcon,
        Vectorfooter
    }
}
</script>