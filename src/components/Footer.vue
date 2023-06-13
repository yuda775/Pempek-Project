<!-- <script>
import vectorfooter from './icons/vectorfooter.vue';
</script> -->

<template>
    <div class="footer-content">
        <img class="logo" src="./icons/pempek.png" alt="brand-logo" width="125">
        <i class="icon" src="./icons/facebook.png"  width="125"></i>
        <p class="alamat">Unnamed Road, Nagrak, Kec. Cangkuang, Kabupaten Bandung, Jawa Barat 40238</p>
        <p>&copy; {{ currentYear }} All rights reserved by Nash<span class="kuning"> Tech</span></p>
    </div>
    <div class="vectorfooter">
        <vectorfooter />
    </div>
</template>

<script>
export default {
    data() {
        return {
            currentYear: new Date().getFullYear()
        };
    }
};
</script>

<style scoped>

.footer-content {
    display: flex;
    align-items: center;
    justify-content: center;
}

.icon {
    color: black;
    margin-top: 500px;
}

.vectorfooter {
    position: absolute;
    right: 100px;
    bottom: 4000px;
}

.kuning{
    color: var(--primary-color);
}

.logo {
    margin-top: 300px;
    position: absolute;
}

.alamat {
    font-style: italic;
    margin-top: 440px;
}

p {
    margin-top: 700px;
    position: absolute;
    font-size: medium;
    text-align: center;
}
</style>
