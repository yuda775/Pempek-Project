<template>
    <div id="carouselExampleDark" class="carousel carousel-dark slide">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active"
                aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" aria-label="Slide 2"></button>
        </div>
        <div class="carousel-inner">
            <div class="carousel-item active" data-bs-interval="10000">
                <div class="row container mx-auto mt-5">
                    <div class="col-lg-5">
                        <div class="main-menu me-2">
                            <img src="assets/products/headlinemenu.jpg" alt="headline menu image">
                            <h2 class="mt-4">Pempek Princess Premium</h2>
                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam debitis veniam, doloribus
                                maxime ad vero?
                            </p>
                        </div>
                    </div>
                    <div class="col-lg-7">
                        <div class="d-flex flex-wrap justify-content-between">
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="carousel-item" data-bs-interval="2000">
                <div class="row container mx-auto mt-5">
                    <div class="col-lg-7">
                        <div class="d-flex flex-wrap justify-content-between">
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                            <div class="sub-menu">
                                <img src="assets/products/adaan.png" width="200">
                                <h2> Adaan</h2>
                                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam, illum.</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-5">
                        <div class="main-menu me-2">
                            <img src="assets/products/pempek-headline2.jpg" alt="headline menu image">
                            <h2 class="mt-4">Pempek Princess Premium</h2>
                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam debitis veniam, doloribus
                                maxime ad vero?
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
</style>
