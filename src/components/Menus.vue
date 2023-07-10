<template>
    <div id="carouselExampleDark" class="carousel carousel-dark slide">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active"
                aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" aria-label="Slide 2"></button>
        </div>
        <div class="carousel-inner container">
            <div class="carousel-item active" data-bs-interval="10000">
                <div class="row mx-auto mt-5">
                    <div class="col-lg-5">
                        <div class="main-menu me-2">
                            <img src="/assets/products/headlinemenu.jpg" alt="headline menu image">
                            <h2 class="mt-4 fw-bold">Pempek Princess Premium</h2>
                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam debitis veniam, doloribus
                                maxime ad vero?
                            </p>
                        </div>
                    </div>
                    <div class="col-lg-7">
                        <div class="d-flex flex-wrap justify-content-between">
                            <div class="sub-menu">
                                <img src="/assets/products/adaan.png" width="200">
                                <h2>Pemepek Adaan</h2>
                                <p>Pempek adaan digoreng langsung setelah dibentuk bulat dari adonan, tanpa melalui tahap
                                    perebusan terlebih dahulu. </p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/kapalselam.png" width="200">
                                <h2> Pemepek Kapal Selam</h2>
                                <p>Pempek kapal selam berisi telur ayam rebus atau telur bebek, pempek ini lebih nikmat bila
                                    disajikan dengan irisan timun.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/keriting.png" width="200">
                                <h2> Pemepek keriting</h2>
                                <p>Pempek tradisional yang menyerupai bola mie dan dibentuk manual dengan tangan.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/kulit.png" width="200">
                                <h2> Pemepek kulit</h2>
                                <p>Pempek kulit biasanya menggunakan campuran tepung dan adonan kulit ikan. Ikan yang paling
                                    sering digunakan adalah ikan tenggiri.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/panggang.png" width="200">
                                <h2> Pemepek Tunu/Panggang</h2>
                                <p>Pempek tunu mirip seperti pempek lenggang karena biasanya diolah dengan dibakar atau
                                    dipanggang. </p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/lenjer.png" width="200">
                                <h2> Pemepek Lenjer</h2>
                                <p>Lenjer juga tidak memiliki isian apapun, sehinggsa bisa dikatakan sebagai versi original
                                    dari pempek. </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="carousel-item" data-bs-interval="2000">
                <div class="row mx-auto mt-5">
                    <div class="col-lg-7">
                        <div class="d-flex flex-wrap justify-content-between">
                            <div class="sub-menu">
                                <img src="/assets/products/pempekdos.png" width="200">
                                <h2> Pempek Dos</h2>
                                <p> Yang membedakan pempek dos adalah bahan utamanya yang tidak menggunakan daging ikan,
                                    biasanya pempek ini memiliki isian pepaya</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/tekwan.png" width="200">
                                <h2> Tekwan</h2>
                                <p>Tekwan dibuat dari adonan pempek lenjer, namun yang membuat tekwan berbeda adalah
                                    disajikan menggunakan kuah sup yang dimasak bersama udang.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/otakotak.png" width="200">
                                <h2> Otak otak</h2>
                                <p>Terbuat dari daging ikan tenggiri cincang yang dibungkus dengan daun pisang, dipanggang,
                                    dan disajikan dengan saus kacang atau kuah asam pedas.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/kemasan.png" width="200">
                                <h2> Pempek kemasan</h2>
                                <p>Pempek kemasan merupakan edisi spesial yang dapat dipesan untuk customer online.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/kerupuk.png" width="200">
                                <h2> Pempek Kerupuk </h2>
                                <p>Pempek ini dibuat karena ketidak sengajaan</p>
                            </div>
                            <div class="sub-menu">
                                <img src="/assets/products/cuko.png" width="200">
                                <h2>Kuah Cuko</h2>
                                <p>Kuah untuk pempek</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-5">
                        <div class="main-menu me-2">
                            <img src="/assets/products/pempek-headline2.jpg" alt="headline menu image">
                            <h2 class="mt-4 fw-bold">Ikan ikan apa yang bikin baper?</h2>
                            <p>Ikan stop loving you.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>

<style scoped>
* {
    box-sizing: border-box;
    /* border: 1px dashed salmon; */
}

p {
    font-style: italic;
}

.main-menu {
    width: auto;
}

img {
    border-radius: 3px;
}

.carousel-item {
    padding: 10px;
}

.row {
    margin: 0;
    padding: 0;
}


.sub-menu {
    width: 200px;
    margin-bottom: 20px;
}

.sub-menu img {
    width: 100%;
    height: 130px;
    max-height: 150px;
    object-fit: cover;
    margin-bottom: 10px;
}

.sub-menu h2 {
    font-size: 18px;
    margin-bottom: 10px;
}

.sub-menu p {
    font-size: 14px;
    color: #777;
}

@media screen and (max-width: 1024px) {
    .sub-menu {
        width: 30%;
    }

    .sub-menu img {
        height: 100px;
    }

    .sub-menu h2 {
        font-size: 14px;
    }

    .sub-menu p {
        font-size: 12px;
    }
}

@media screen and (max-width: 991px) {
    .sub-menu {
        width: 30%;
    }

    .sub-menu img {
        height: 70px;
    }

    .sub-menu h2 {
        font-size: 13px;
    }

    .sub-menu p {
        font-size: 12px;
    }
}
</style>
