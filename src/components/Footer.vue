<!-- <script>
import vectorfooter from './icons/vectorfooter.vue';
</script> -->

<template>
    <div class="footer-content text-center">
        <img class="logo mx-auto d-block" src="./icons/pempek.png" alt="brand-logo" width="125">
        <p class="alamat fw-bold">Unnamed Road, Nagrak, Kec. Cangkuang, Kabupaten Bandung, Jawa Barat 40238</p>
        <div class="social-icons">
            <a class="icon" href="#"><font-awesome-icon :icon="['fab', 'facebook']" /></a>
            <a class="icon" href="#"><font-awesome-icon :icon="['fab', 'twitter']" /></a>
            <a class="icon" href="#"><font-awesome-icon :icon="['fab', 'instagram']" /></a>
        </div>
        <p class="mt-3">&copy; 2023 All rights reserved by Nash<span class="kuning"> Tech</span></p>
    </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { library } from '@fortawesome/fontawesome-svg-core'
import { faFacebook, faTwitter, faInstagram } from '@fortawesome/free-brands-svg-icons'

library.add(faFacebook, faTwitter, faInstagram)

export default {
  components: {
    FontAwesomeIcon
  }
}
</script>

<style scoped>

.footer-content{
    margin-top: 200px;
}
.icon:hover{
    color: var(--primary-color);
}
.icon{
    font-size: 25px;
    margin-inline: 5px;
    border-radius: 100%;
    color: var(--secondary-color);
}

/* .vectorfooter {
    position: absolute;
    right: 100px;
    bottom: 4000px;
} */

.kuning{
    color: var(--primary-color);
}

.alamat {
    margin-top: 30px;
    font-weight: bold;
    font-style: italic;
}
</style>
