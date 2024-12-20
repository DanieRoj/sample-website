# sample-website

<h4> CSS CODE </h4>

```css 

/* TABLE OF CONTENTS */
/* ------------------
1. General
2. Navbar
3. Slider
4. About
5. Rooms
6. Services
6. Team
7. Gallery
8. Price
9. Blog
10. Footer
-------------------- */

/* 1 General */
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    /* Background Color */
    --primary-color: #021832;
    --secondary-color: #caa169;
    --bg-color: #f4f4f4;
    --bg-white: #fff;
    --bg-black: #000;

    /* Text Style */
    --primary-font: 'Poppins', sans-serif;
    --secondary-font: 'Oswald', sans-serif;
    --primary-text: #021832;
    --secondary-text: #caa169;
    --text-white: #fff;
    --text-black: #151515;
    --text-gray: #e4e4e4;
}

body {
    font-family: var(--primary-font);
    background-color: var(--bg-white);
}

a {
    text-decoration: none;
}

::-webkit-scrollbar {
    width: .375rem;
}

::-webkit-scrollbar-track {
    background: var(--secondary-color);
}

::-webkit-scrollbar-thumb {
    background: var(--primary-color);
}

/*============================================*/

.wrapper
{
    padding: 3.215rem 0;
}

.main-btn
{
    font-size: 1rem;
    font-weight: 500;
    color: var(--primary-color);
    text-transform: uppercase;
    background-color: transparent;
    border: 0.0625rem solid var(--primary-color);
    padding: 0.375rem 1.875rem;
    border-radius: 3.125rem;
    line-height: 1.75rem;
    display: inline-block;
    transition: all 0.3s ease-out 0s;
}

/*navbar*/

.main-btn:hover
{
    background-color: var(--secondary-color);
    border-color: var(--secondary-color);
    color: var(--text-white);
}

h1{
    font-size: 3.75rem;
    line-height: 4.25rem;
    font-weight: 700;
    color: var(--text-white);
    margin-bottom: 1.25rem;
    text-transform: uppercase;
    font-family: var(--secondary-font);
}

h2{
    font-size: 2.25rem;
    line-height: 4.25rem;
    font-weight: 700;
    color: var(--text-white);
    margin-bottom: 1.25rem;
    text-transform: uppercase;
    font-family: var(--secondary-font);
}

h3 {
    margin-bottom: 1.875rem;
    line-height: 2.875rem;
    font-weight: 700;
    font-size: 2.25rem;
    color: var(--primary-text);
    font-family: var(--secondary-font);
}

h4 {
    margin-bottom: 1.5rem;
    line-height: 2.875rem;
    font-weight: 700;
    font-size: 2.25rem;
    color: var(--primary-text);
    font-family: var(--secondary-font);
}


h3 span
{
    color: var(--secondary-color);
}

h5
{
    font-size: 1.5rem;
    line-height: 1;
    color: var(--primary-text);
    font-weight: 500;
    font-family: var(--secondary-font);
}

h6
{
    font-size: 0.875rem;
    color: var(--primary-text);
    margin-bottom: 0.9375rem;
    text-transform: uppercase;
    font-weight: 300;
    font-family: var(--secondary-font);
}

p {
    font-size: 1rem;
    color: var(--text-black);
    line-height: 1.625rem;
}

.section-title:after
{
    content: '';
    background-image: url("../images/title-icon.webp");
    background-position: center center;
    background-repeat: no-repeat;
    display: block;
    margin-top: -0.9375rem;
    height: 0.9375rem;
}

/* 2 Navbar */

.header_wrapper .navbar {
    padding: .9375rem 0;
    background-color: var(--bg-white);
    -webkit-box-shadow: 0 .5rem .375rem -0.375rem rgb(0 0 0 / 40%);
    box-shadow: 0 .5rem .375rem -0.375rem rgb(0 0 0 / 40%);
    -webkit-transition: background 0s ease-in-out 0s, margin-top 0s ease-in-out 0s, opacity 0s ease-in-out 0s;
    transition: background 0s ease-in-out 0s, margin-top 0s ease-in-out 0s, opacity 0s ease-in-out 0s;
}

.header_wrapper .navbar-toggler {
    border: 0;
    color: var(--primary-text);
    line-height: 2;
}

.header_wrapper .navbar-toggler:focus {
    box-shadow: none;
}

.header_wrapper .nav-item
{
    margin: 0 0.625rem;
}

.header_wrapper .nav-item .nav-link
{
    font-size: 1rem;
    font-weight: 500;
    color: var(--primary-text);
    display: inline-block;
}


.header_wrapper .nav-item .nav-link.active,
.header_wrapper .nav-item .nav-link:hover {
    color: var(--secondary-text);
}

.navbar.header-scrolled {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 999;
    background-color: rgba(255, 255, 255, .85);
    -webkit-animation: 500ms ease-in-out 0s normal none 1 running fadeInDown;
    animation: 500ms ease-in-out 0s normal none 1 running fadeInDown;
}

@keyframes fadeInDown {
    0% {
        top: -30%;
    }

    50% {
        top: -15%;
    }

    100% {
        top: 0;
    }
}

/* 3 Banner */
.banner_wrapper {
    height: 40.625rem;
}

.banner_wrapper .swiper {
    width: 100%;
    height: 100%;
}

.banner_wrapper .swiper-slide {
    width: 100%;
    height: 100%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
}

.banner_wrapper .swiper-slide::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: var(--bg-black);
    opacity: 0.5;
    z-index: 0;
}


.banner_wrapper .swiper-pagination-bullets .swiper-pagination-bullet {
    width: .9375rem;
    height: .9375rem;
    background-color: var(--secondary-color);
    border: .0625rem solid var(--bg-white);
}

.banner_wrapper .swiper .slide-caption {
    height: 100%;
    position: relative;
    z-index: 99;
    display: flex;
    align-items: center;
    justify-content: center;
}


.banner_wrapper .swiper .slide-caption p{
   max-width: 37.5rem;
   margin: 0 auto;
   color: var(--text-white);
}

.booking-area
{
    background: var(--bg-white);
    box-shadow: 0 .625rem .9375rem 0 rgb(0 0 0 / 10%);
    margin-top: -4rem;
    padding: 3.125rem 1.875rem;
    position: relative;
    z-index: 2;
}

/*About section*/

.about_wrapper {
    padding-top: 9.375rem;
}

/* Room */
.rooms_wrapper .room-item
{
    position: relative;
    overflow: hidden;
}

.rooms_wrapper .room-item img {
    width:100%;
    -webkit-transition: all 400ms ease-in 0s;
    transition: all 400ms ease-in 0s;
}

.rooms_wrapper .room-item:hover img {
    -webkit-transform: scale3d(1.05, 1.05, 1.05);
    transform: scale3d(1.05, 1.05, 1.05);
}

.rooms_wrapper .room-item::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: var(--bg-black);
    opacity: 0;
    z-index: 1;
    -webkit-transition: all 400ms ease-in 0s;
    transition: all 400ms ease-in 0s;
}

.rooms_wrapper .room-item:hover::before {
    opacity: 0.6;
}

.rooms_wrapper .room-item-wrap {
    left: 1.875rem;
    right: 1.875rem;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 1;
}

.rooms_wrapper .room-item .room-content {
    border: .125rem solid #fff;
    padding: 5rem 1.875rem;
    -webkit-transform: scale3d(1.2, 1.2, 1.2);
    transform: scale3d(1.2, 1.2, 1.2);
    -webkit-transition: all 500ms ease-in 0s;
    transition: all 500ms ease-in 0s;
    opacity: 0;
}

.rooms_wrapper .room-item:hover .room-content {
    opacity: 1;
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
}

/* 6 services */

.service-item-wrap {
    background-color: var(--bg-color);
}

.service-menu-area ul li a {
    display: block;
    margin-bottom: 2.8125rem;
}

.service-menu-area ul li a .service-icon {
    height: 5.625rem;
    width: 5.625rem;
    background-color: var(--secondary-color);
    line-height: 5.625rem;
    text-align: center;
    border-radius: 100%;
    float: left;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
}

.service-menu-area ul li a .service-icon:hover,
.service-menu-area ul li a.active .service-icon {
    background-color: #021832;
    color: #fff;
    box-shadow: 0 .125rem 1.25rem rgb(34 30 31 / 40%);
}

.service-menu-area ul li:nth-child(1) {
    margin-left: 0.5625rem;
}

.service-menu-area ul li:nth-child(2) {
    margin-left: -2.9375rem;
}

.service-menu-area ul li:nth-child(3) {
    margin-left: -6.375rem;
}

.service-menu-area ul li:nth-child(4) {
    margin-left: -8.8125rem;
}

.service-menu-area ul li a p,
.service-menu-area ul li a h5 {
    padding-left: 6.875rem;
    display: block;
    text-align: left;
}

.service-menu-area ul li a p span {
    color: var(--secondary-text)
}

/* 7 counter */


.counter {
    background-image: url('../images/counter-bg.webp');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    padding: 3.125rem;
    position: relative;
}

.counter::before {
    position: absolute;
    content: "";
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: var(--bg-black);
    opacity: 0.5;
    z-index: 1;
}

.counter h1,
.counter p {
    position: relative;
    z-index: 3;
    color: var(--text-white)
}



/*7 Team Section */

.team_wrapper .card {
    position: relative;
    overflow: hidden;
}

.team_wrapper .team-info {
    background-color: var(--secondary-color);
    position: absolute;
    width: 100%;
    bottom: 0;
    text-align: center;
    padding: 1.25rem;
    margin-bottom: -4.6875rem;
    transition: all 0.3s ease-in-out;
}

.team_wrapper .card:hover .team-info {
    margin-bottom: 0;
}

.team_wrapper .team-info h5,
.team_wrapper .team-info p {
    color: var(--text-white);
}

.team_wrapper .team-info .social-network {
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    padding: 1.25rem;
    margin: 1.25rem -1.25rem -1.25rem;
    background-color: var(--primary-color);
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.team_wrapper .team-info .social-network li a {
    width: 2rem;
    height: 2rem;
    line-height: 2rem;
    display: block;
    border-radius: 50%;
    font-size: .9375rem;
    color: var(--text-white);
    border: .0625rem solid var(--bg-white)
}


/*8 Gallery Section */

.gallery-item {
    box-shadow: 0 0 .1875rem rgba(0, 0, 0, 0.3);
    overflow: hidden;
    position: relative;
}

.gallery-item:before,
.gallery-item:after,
.gallery-item .gallery-item-content:before,
.gallery-item .gallery-item-content:after {
    content: "";
    width: 50%;
    height: 50%;
    background: rgba(0, 0, 0, 0.8);
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    -webkit-transition: all 0.5s ease 0s;
    transition: all 0.5s ease 0s;
}

.gallery-item:after {
    top: 50%;
}

.gallery-item:hover:after {
    top: 0;
    opacity: 1;
}

.gallery-item:hover:before {
    left: 50%;
    opacity: 1;
}

.gallery-item .gallery-item-content {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    text-align: center;
    opacity: 0;
    z-index: 1;
    -webkit-transition: all 0.3s ease 0s;
    transition: all 0.3s ease 0s;
}

.gallery-item:hover .gallery-item-content {
    opacity: 1;
}

.gallery-item .gallery-item-content:before,
.gallery-item .gallery-item-content:after {
    top: 0;
    left: 50%;
    z-index: -1;
}

.gallery-item:hover .gallery-item-content:before {
    top: 50%;
    opacity: 1;
}

.gallery-item .gallery-item-content:after {
    top: 50%;
}

.gallery-item:hover .gallery-item-content:after {
    left: 0;
    opacity: 1;
}

/*9 pricing section */

.price_wrapper .card {
    box-shadow: 0 .125rem .25rem rgb(34 30 31 / 40%);
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    cursor: pointer;
}

.price_wrapper .card:hover {
    background-color: var(--secondary-color);
}

.price_wrapper .card:hover h3,
.price_wrapper .card:hover h5,
.price_wrapper .card:hover p {
    color: var(--text-white);
}

.price_wrapper .card:hover .main-btn {
    color: var(--text-white);
    border-color: var(--bg-white)
}


/*10 blog */
.blog-content {
    margin: -5rem 0 0 4.375rem;
    box-shadow: 0 .125rem .25rem rgb(34 30 31 / 40%);
}

.our-partner-slider {
    background-color: var(--bg-color);
    padding: 3.125rem 0;
}


/*------================== 11 footer ===============-------- */

.footer_wrapper {
    background-color: var(--bg-black);
}

.footer_wrapper h5 {
    color: var(--text-white);
    margin-bottom: 1.25rem;
}

.footer_wrapper ul li {
    margin-bottom: .5rem;
    list-style: none;
}

.footer_wrapper .contact-info li a{
    color: var(--secondary-color)
}

.footer_wrapper .link-widget li a,
.footer_wrapper p {
    color: var(--text-gray);
    font-size: .875rem;
    padding-left:1.5rem;
    position: relative;
    -webkit-transition: all 0.3s ease-out 0s;
    transition: all 0.3s ease-out 0s;
}

.footer_wrapper .link-widget li a::before {
    content: '\f105';
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    position: absolute;
    left: 0.3rem;
    top: 50%;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
}

.footer_wrapper .link-widget li a:hover {
    margin-left: .625rem;
    color: var(--secondary-text);
}

.footer_wrapper .social-network a {
    width: 2.1875rem;
    height: 2.1875rem;
    margin: .5rem;
    line-height:2rem;
    font-size: .875rem;
    display: inline-block;
    border: .125rem solid var(--text-gray);
    color: var(--text-gray);
    text-align: center;
    border-radius: 100%;
    -webkit-transition: all 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
    transition: all 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
}

.footer_wrapper .social-network a:hover {
    background-color: var(--secondary-color);
    border-color: var(--secondary-color);
    color: var(--text-white);
    box-shadow: 0 .625rem .9375rem 0 rgb(0 0 0 / 10%);
    transform: translateY(-0.1875rem);
}

.footer_wrapper .form-control:focus {
    outline: none;
    box-shadow: none;
    border-color: var(--secondary-color);
}

.footer_wrapper .copyright-section {
    background-color: var(--primary-color);
    padding: 1.25rem 0 .3125rem;
    text-align: center;
}


.footer_wrapper .copyright-section a {
    color: var(--secondary-text);
}

```

<h4> HTML CODE </h4>

```html

```html


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel Website Design by Code4education</title>

    <!-- FAVICON -->
    <link rel="icon" type="image/png" href="images/favicon.png">

    <!-- Bootstrap 5 CDN Links -->
    <link rel="stylesheet" href="css/bootstrap/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

    <!-- Link Swiper's CSS -->
    <link rel="stylesheet" href="css/swiper/swiper-bundle.min.css">

    <!-- Custom File's Link -->
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/responsive-style.css">

</head>
<body data-bs-spy="scroll" data-bs-target=".navbar" data-bs-offset="100">



<header class="header_wrapper">
    <nav class="navbar navbar-expand-lg">
        <div class="container">

            <a class="navbar-brand" href="#">
                <img src="images/logo.png" alt="logo" class="img-fluid">
            </a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <!--<span class="navbar-toggler-icon"></span>-->
                <i class="fas fa-stream navbar-toggler-icon"></i>
            </button>



            <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                <ul class="navbar-nav menu-navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#phone">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#rooms">Rooms</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#services">Services</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#team">Team</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#gallery">Gallery</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#price">Price</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#blog">Blog</a>
                    </li>

                    <li class="nav-item mt-3 mt-lg-0">
                        <a class="main-btn" href="#">Book Now</a>
                    </li>

                </ul>
            </div>
        </div>
    </nav>
</header>



<!--Banner section-->

<section id="home" class="banner_wrapper p-0">
    <div class="swiper mySwiper wrapper">
        <div class="swiper-wrapper">
            <!--======= First Slider ========-->
            <div class="swiper-slide" style="background-image: url(./images/slider/slider1.webp)">
                <div class="slide-caption text-center">
                    <div>
                        <h1>welcome to hotel in Dubai</h1>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
                            incididunt ut labore et dolore magna aliqua. Ut enim </p>
                    </div>
                </div>
            </div>

            <!--======= Second Slider ========-->
            <div class="swiper-slide" style="background-image: url(./images/slider/slider2.webp)">
                <div class="slide-caption text-center">
                    <div>
                        <h1>welcome to hotel in Dubai</h1>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
                            incididunt ut labore et dolore magna aliqua. Ut enim </p>
                    </div>
                </div>
            </div>

            <!--======= Third Slider ========-->
            <div class="swiper-slide" style="background-image: url(./images/slider/slider1.webp)">
                <div class="slide-caption text-center">
                    <div>
                        <h1>welcome to hotel in Dubai</h1>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
                            incididunt ut labore et dolore magna aliqua. Ut enim </p>
                    </div>
                </div>
            </div>

        </div>
        <div class="swiper-pagination"></div>
    </div>

    <!--============= Booking Area =============-->
    <div class="container booking-area">
        <form class="row">
            <div class="col-lg mb-3 mb-lg-0">
                <input type="date" class="form-control" placeholder="Date">
            </div>
            <div class="col-lg mb-3 mb-lg-0">
                <input type="date" class="form-control" placeholder="Date">
            </div>
            <div class="col-lg mb-3 mb-lg-0">
                <select class="form-select">
                    <option selected>Adults</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5</option>
                    <option value="6">6</option>
                </select>
            </div>
            <div class="col-lg mb-3 mb-lg-0">
                <select class="form-select">
                    <option selected>Children</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5</option>
                    <option value="6">6</option>
                </select>
            </div>
            <div class="col-lg mb-3 mb-lg-0">
                <button type="submit" class="main-btn rounded-2 px-lg-3">Check Availability</button>
            </div>
        </form>
    </div>
</section>


<!-- About section -->
<section id="about" class="about_wrapper">
    <div class="container wrapper">
        <div class="row flex-lg-row flex-column-reverse ">
            <div class="col-lg-6 text-center text-lg-start">
                <h3>Welcome to <span>Hotel <br class="d-none d-lg-block">
                            the haven</span> of your weekend</h3>
                <p>lorum luptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni
                    dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum
                    quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius</p>
                <p>lorum luptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni
                    dolores eos qui ratione voluptatem</p>
                <a href="#" class="main-btn mt-4">Explore</a>
            </div>
            <div class="col-lg-6 mb-4 mb-lg-0 ps-lg-4 text-center">
                <img decoding="async" src="images/about-img.svg" class="img-fluid" alt="About Us">
            </div>
        </div>
    </div>
</section>
<!-- About section exit -->


<!-- Rooms section -->
<section id="rooms" class="rooms_wrapper">
    <div class="container-fluid wrapper">

        <!--=========================== Title ===============================-->
        <div class="row">
            <div class="col-sm-12 section-title text-center mb-5">
                <h6>What I can do for you</h6>
                <h3>Our Favorite Rooms</h3>
            </div>
        </div>

        <!--===========================  images  ===============================-->

        <div class="row m-0">

            <div class="col-md-4 mb-4 mb-lg-0">
                <div class="room-item">
                    <img decoding="async" src="./images/room/room1.webp" class="img-fluid">
                    <div class="room-item-wrap">
                        <div class="room-content">
                            <h5 class="text-white mb-lg-5 text-decoration-underline">Royal Suit</h5>
                            <p class="text-white">Discover five of our favourite dresses from our new collection that
                                are destined to be worn and loved immediately</p>
                            <p class="text-white fw-bold mt-lg-4">$220 / Per Night</p>
                            <a class="main-btn border-white text-white mt-lg-5" href="#">Book now</a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-md-4 mb-4 mb-lg-0">
                <div class="room-item">
                    <img decoding="async" src="./images/room/room2.webp" class="img-fluid">
                    <div class="room-item-wrap">
                        <div class="room-content">
                            <h5 class="text-white mb-lg-5 text-decoration-underline">Royal Suit</h5>
                            <p class="text-white">Discover five of our favourite dresses from our new collection that
                                are destined to be worn and loved immediately</p>
                            <p class="text-white fw-bold mt-lg-4">$220 / Per Night</p>
                            <a class="main-btn border-white text-white mt-lg-5" href="#">Book now</a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-md-4 mb-4 mb-lg-0">
                <div class="room-item">
                    <img decoding="async" src="./images/room/room3.webp" class="img-fluid">
                    <div class="room-item-wrap">
                        <div class="room-content">
                            <h5 class="text-white mb-lg-5 text-decoration-underline">Royal Suit</h5>
                            <p class="text-white">Discover five of our favourite dresses from our new collection that
                                are destined to be worn and loved immediately</p>
                            <p class="text-white fw-bold mt-lg-4">$220 / Per Night</p>
                            <a class="main-btn border-white text-white mt-lg-5" href="#">Book now</a>
                        </div>
                    </div>
                </div>
            </div>


        </div>
        <!--////////////-->
    </div>
</section>
<!-- Rooms Section Exit -->



<!-- Services section -->
<section id="services" class="services_wrapper">
    <div class="container wrapper">

        <!--===================  title ========================-->

        <div class="row">
            <div class="col-sm-12 section-title text-center mb-5">
                <h6>We Are Here For You</h6>
                <h3>Our Awesome Services</h3>
            </div>
        </div>

        <!--===================================================-->


        <div class="row align-items-center service-item-wrap">


            <div class="col-lg-7 p-lg-0">
                <!--Service Area Start-->
                <div class="tab-content" id="myTabContent">

                    <div class="tab-pane fade active show" id="spa" role="tabpanel">
                        <img decoding="async" src="./images/services/service1.webp" alt="">
                    </div>

                    <div class="tab-pane fade" id="restaurent" role="tabpanel">
                        <img decoding="async" src="./images/services/service2.webp" alt="">
                    </div>

                    <div class="tab-pane fade" id="swimming" role="tabpanel">
                        <img decoding="async" src="images/services/service3.webp" alt="">
                    </div>

                    <div class="tab-pane fade" id="conference" role="tabpanel">
                        <img decoding="async" src="./images/services/service6.webp" alt="">
                    </div>

                </div>
                <!--Service Area End-->
            </div>



            <div class="col-lg-5 position-relative">
                <!--Service Tab Menu Area Start-->
                <div class="service-menu-area">
                    <ul class="nav">


                        <li>
                            <a data-bs-toggle="tab" href="#spa" class="active">
                                    <span class="service-icon">
                                        <img decoding="async" src="./images/services/service-icon1.webp" alt="">
                                    </span>
                                <h5>Spa, beauty & Health</h5>
                                <p><span>Spa and beauty </span>luptatem quia voluptas sit aspernatur aut odit aut
                                    fugit, sed quia </p>
                            </a>
                        </li>


                        <li>
                            <a data-bs-toggle="tab" href="#restaurent">
                                    <span class="service-icon">
                                        <img decoding="async" src="./images/services/service-icon2.webp" alt="">
                                    </span>
                                <h5>Restaurant</h5>
                                <p><span>Restaurant</span> lup provide grro tatem quia voluptas sit aspernatur aut
                                    odit aut fugit, </p>
                            </a>
                        </li>


                        <li>
                            <a data-bs-toggle="tab" href="#swimming">
                                    <span class="service-icon">
                                        <img decoding="async" src="./images/services/service-icon3.webp" alt="">
                                    </span>
                                <h5>Swimming Pool</h5>
                                <p><span>Swimming</span> pool luptatem quia voluptas sit aspernatur aut odit aut
                                    fugit, sed quia </p>
                            </a>
                        </li>


                        <li>
                            <a data-bs-toggle="tab" href="#conference">
                                    <span class="service-icon">
                                        <img decoding="async" src="./images/services/service-icon4.webp" alt="">
                                    </span>
                                <h5>Conference Hall</h5>
                                <p><span>Conference</span> luptatem quia voluptas sit aspernatur aut odit aut fugit,
                                    sed quia </p>
                            </a>
                        </li>


                    </ul>
                </div>
                <!--Service Tab Menu Area End-->
            </div>
        </div>
    </div>


    <!--==================== Count section  ==========================-->


    <div class="counter mt-5">
        <div class="container">
            <div class="row text-center">

                <div class="col-md-3 mb-lg-0 mb-md-0 mb-5">
                    <h1>
                        <span id="count1"></span>+
                    </h1>
                    <p>Happy Clients</p>
                </div>

                <div class="col-md-3 mb-lg-0 mb-md-0 mb-5">
                    <h1>
                        <span id="count2"></span>+
                    </h1>
                    <p>New Friendships</p>
                </div>

                <div class="col-md-3 mb-lg-0 mb-md-0 mb-5">
                    <h1>
                        <span id="count3"></span>+
                    </h1>
                    <p>Five Start Ratings</p>
                </div>

                <div class="col-md-3 mb-lg-0 mb-md-0 mb-5">
                    <h1>
                        <span id="count4"></span>+
                    </h1>
                    <p>Served Breakfast</p>
                </div>

            </div>
        </div>
    </div>

</section>
<!-- Services section Exit -->


<!-- Team section -->
<section id="team" class="team_wrapper">
    <div class="container wrapper">


        <!--==================== title =============================-->

        <div class="row">
            <div class="col-sm-12 section-title text-center mb-5">
                <h6>What I can do for you</h6>
                <h3>Our Special Staff</h3>
            </div>
        </div>





        <div class="row">

            <!--================ team 001 =====================-->

            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-0 rounded-3">
                    <img decoding="async" src="images/team/team1.webp" class="img-fluid rounded-3" />
                    <div class="team-info">
                        <h5>Shirley Gibson</h5>
                        <p>Manager</p>
                        <ul class="social-network">
                            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                            <li><a href="#"><i class="fab fa-google-plus-g"></i></a></li>
                            <li><a href="#"><i class="fab fa-vimeo-v"></i></a></li>
                        </ul>
                    </div>
                </div>
            </div>

            <!--================ team 002 =====================-->


            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-0 rounded-3">
                    <img decoding="async" src="images/team/team2.webp" class="img-fluid rounded-3" />
                    <div class="team-info">
                        <h5>Ronald Long</h5>
                        <p>Chif Reciption Officer</p>
                        <ul class="social-network">
                            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                            <li><a href="#"><i class="fab fa-google-plus-g"></i></a></li>
                            <li><a href="#"><i class="fab fa-vimeo-v"></i></a></li>
                        </ul>
                    </div>
                </div>
            </div>


            <!--================ team 003 =====================-->


            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-0 rounded-3">
                    <img decoding="async" src="images/team/team3.webp" class="img-fluid rounded-3" />
                    <div class="team-info">
                        <h5>Ashley Sanchez</h5>
                        <p>Master Chef</p>
                        <ul class="social-network">
                            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                            <li><a href="#"><i class="fab fa-google-plus-g"></i></a></li>
                            <li><a href="#"><i class="fab fa-vimeo-v"></i></a></li>
                        </ul>
                    </div>
                </div>
            </div>

            <!--================ team 004 =====================-->


            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-0 rounded-3">
                    <img decoding="async" src="images/team/team4.webp" class="img-fluid rounded-3" />
                    <div class="team-info">
                        <h5>Jessica Watson</h5>
                        <p>Housekeeping</p>
                        <ul class="social-network">
                            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                            <li><a href="#"><i class="fab fa-google-plus-g"></i></a></li>
                            <li><a href="#"><i class="fab fa-vimeo-v"></i></a></li>
                        </ul>
                    </div>
                </div>
            </div>



        </div>


    </div>
</section>
<!-- Team Section Exit  -->


<!-- Gallery section -->

<section id="gallery" class="gallery_wrapper">
    <div class="container wrapper">

        <!--=================== main title ===========================-->

        <div class="row">
            <div class="col-sm-12 section-title text-center mb-5">
                <h6>Best Pictures Of Our Hotel</h6>
                <h3>Our Gallery</h3>
            </div>
        </div>


        <div class="row g-0">

            <!--=================== image 001 ===========================-->

            <div class="col-lg-3 col-md-6 gallery-item">
                <img decoding="async" src="./images/gallery/1.webp" class="img-fluid w-100">
                <div class="gallery-item-content"></div>
            </div>

            <!--=================== image 002 ===========================-->

            <div class="col-lg-3 col-md-6 gallery-item">
                <img decoding="async" src="./images/gallery/2.webp" class="img-fluid w-100">
                <div class="gallery-item-content"></div>
            </div>

            <!--=================== image 003 ===========================-->

            <div class="col-lg-3 col-md-6 gallery-item">
                <img decoding="async" src="./images/gallery/3.webp" class="img-fluid w-100">
                <div class="gallery-item-content"></div>
            </div>

            <!--=================== image 004 ===========================-->

            <div class="col-lg-3 col-md-6 gallery-item">
                <img decoding="async" src="./images/gallery/4.webp" class="img-fluid w-100">
                <div class="gallery-item-content"></div>
            </div>


            <!--=================== image 005 ===========================-->

            <div class="col-md-6 gallery-item">
                <img decoding="async" src="./images/gallery/5.webp" class="img-fluid w-100">
                <div class="gallery-item-content"> </div>
            </div>

            <!--=================== image 006 ===========================-->

            <div class="col-md-6 gallery-item">
                <img decoding="async" src="./images/gallery/6.webp" class="img-fluid w-100">
                <div class="gallery-item-content"> </div>
            </div>

        </div>


    </div>
</section>

<!-- Gallery Section Exit -->


<!-- Pricing section -->
<section id="price" class="price_wrapper">
    <div class="container wrapper">

        <!--============================ main title =============================-->

        <div class="row">
            <div class="col-sm-12 section-title text-center mb-5">
                <h6>Best & Affordable Price for you</h6>
                <h3>Our Pricing</h3>
            </div>
        </div>



        <div class="row">
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-4 text-center rounded-3">
                    <h5 class="text-decoration-underline mb-4">Economic</h5>
                    <ul class="list-unstyled">
                        <li>
                            <p>Flight Ticket(2)</p>
                        </li>
                        <li>
                            <p>Music Concert (30% Off)</p>
                        </li>
                        <li>
                            <p>Restaurant (Snacks)</p>
                        </li>
                        <li>
                            <p>Face Make(No)</p>
                        </li>
                    </ul>
                    <hr />
                    <h3>$150<sub class="fs-6 fw-normal">/NIGHT</sub></h3>
                    <a href="#" class="main-btn">Sign Up</a>
                </div>
            </div>
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-4 text-center rounded-3">
                    <h5 class="text-decoration-underline mb-4">Economic</h5>
                    <ul class="list-unstyled">
                        <li>
                            <p>Flight Ticket(2)</p>
                        </li>
                        <li>
                            <p>Music Concert (30% Off)</p>
                        </li>
                        <li>
                            <p>Restaurant (Snacks)</p>
                        </li>
                        <li>
                            <p>Face Make(No)</p>
                        </li>
                    </ul>
                    <hr />
                    <h3>$150<sub class="fs-6 fw-normal">/NIGHT</sub></h3>
                    <a href="#" class="main-btn">Sign Up</a>
                </div>
            </div>
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-4 text-center rounded-3">
                    <h5 class="text-decoration-underline mb-4">Economic</h5>
                    <ul class="list-unstyled">
                        <li>
                            <p>Flight Ticket(2)</p>
                        </li>
                        <li>
                            <p>Music Concert (30% Off)</p>
                        </li>
                        <li>
                            <p>Restaurant (Snacks)</p>
                        </li>
                        <li>
                            <p>Face Make(No)</p>
                        </li>
                    </ul>
                    <hr />
                    <h3>$150<sub class="fs-6 fw-normal">/NIGHT</sub></h3>
                    <a href="#" class="main-btn">Sign Up</a>
                </div>
            </div>
            <div class="col-lg-3 col-md-6 mb-4">
                <div class="card p-4 text-center rounded-3">
                    <h5 class="text-decoration-underline mb-4">Economic</h5>
                    <ul class="list-unstyled">
                        <li>
                            <p>Flight Ticket(2)</p>
                        </li>
                        <li>
                            <p>Music Concert (30% Off)</p>
                        </li>
                        <li>
                            <p>Restaurant (Snacks)</p>
                        </li>
                        <li>
                            <p>Face Make(No)</p>
                        </li>
                    </ul>
                    <hr />
                    <h3>$150<sub class="fs-6 fw-normal">/NIGHT</sub></h3>
                    <a href="#" class="main-btn">Sign Up</a>
                </div>
            </div>
        </div>
    </div>
</section>
<!-- Pricing Section Exit  -->



<!-- Blog section -->
<section id="blog" class="blog_wrapper pb-0">
    <div class="container wrapper">

        <!--====================== title =======================-->

        <div class="row">
            <div class="col-sm-12 section-title text-center mb-5">
                <h6>Say Hello TO Our Visiters</h6>
                <h3>Our Blog</h3>
            </div>
        </div>

        <!--Two section-->


        <div class="row">

            <div class="col-md-6 mb-4">
                <div class="card p-0 border-0 rounded-0">
                    <img decoding="async" src="images/blog/blog1.webp" alt="">
                    <div class="blog-content bg-white p-4">
                        <h5 class="text-decoration-underline mb-4">Relax Zone</h5>
                        <h6>By Admin - February 18, 2018</h6>
                        <p class="mt-2">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, nostrum.
                        </p>
                        <a href="#" class="main-btn mt-2">Read More</a>
                    </div>
                </div>
            </div>

            <div class="col-md-6 mb-4">
                <div class="card p-0 border-0 rounded-0">
                    <img decoding="async" src="images/blog/blog2.webp" alt="">
                    <div class="blog-content bg-white p-4">
                        <h5 class="text-decoration-underline mb-4">Relax Zone</h5>
                        <h6>By Admin - February 18, 2018</h6>
                        <p class="mt-2">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, nostrum.
                        </p>
                        <a href="#" class="main-btn mt-2">Read More</a>
                    </div>
                </div>
            </div>


        </div>
    </div>


    <!--==================== slider =====================-->


    <div class="our-partner-slider mt-5">
        <div class="container swiper our-partner">
            <div class="swiper-wrapper">
                <div class="swiper-slide"><img decoding="async" src="images/partners/brand1.webp"></div>
                <div class="swiper-slide"><img decoding="async" src="images/partners/brand2.webp"></div>
                <div class="swiper-slide"><img decoding="async" src="images/partners/brand3.webp"></div>
                <div class="swiper-slide"><img decoding="async" src="images/partners/brand4.webp"></div>
                <div class="swiper-slide"><img decoding="async" src="images/partners/brand5.webp"></div>
                <div class="swiper-slide"><img decoding="async" src="images/partners/brand6.webp"></div>
            </div>
        </div>
    </div>


</section>
<!-- Blog Section Exit  -->


<!-- Footer section -->
<section id="contact" class="footer_wrapper mt-3 mt-md-0 pb-0">
    <div class="container pb-3 wrapper">
        <div class="row">
            <div class="col-lg-3 col-md-6">
                <h5>Hotel Location</h5>
                <p class="ps-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dignissim erat ut laoreet
                    pharetra....</p>
                <div class="contact-info">
                    <ul class="list-unstyled">
                        <li><a href="#"><i class="fa fa-home me-3"></i> No. 96, South City, London</a></li>
                        <li><a href="#"><i class="fa fa-phone me-3"></i>+1 222 3333</a></li>
                        <li><a href="#"><i class="fa fa-envelope me-3"></i>info@example.com</a></li>
                    </ul>
                </div>
            </div>
            <div class="col-lg-3 col-md-6">
                <h5>More Links</h5>
                <ul class="link-widget p-0">
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Our Office</a></li>
                    <li><a href="#">Delivery</a></li>
                    <li><a href="#">Our Store</a></li>
                    <li><a href="#">Guarantee</a></li>
                    <li><a href="#">Buy Gift Card</a></li>
                    <li><a href="#">Return Policy</a></li>
                </ul>
            </div>
            <div class="col-lg-3 col-md-6">
                <h5>Demo Links</h5>
                <ul class="link-widget p-0">
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Our Office</a></li>
                    <li><a href="#">Delivery</a></li>
                    <li><a href="#">Our Store</a></li>
                    <li><a href="#">Guarantee</a></li>
                    <li><a href="#">Buy Gift Card</a></li>
                    <li><a href="#">Return Policy</a></li>
                </ul>
            </div>
            <div class="col-lg-3 col-md-6">
                <h5>Newsletter</h5>
                <div class="form-group mb-4">
                    <input type="email" class="form-control bg-transparent" placeholder="enter your email here">
                    <button type="submit" class="main-btn rounded-2 mt-3 border-white text-white">Subscribe</button>
                </div>
                <h5>Stay Connected</h5>
                <ul class="social-network d-flex align-items-center p-0">
                    <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                    <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                    <li><a href="#"><i class="fab fa-google-plus-g"></i></a></li>
                    <li><a href="#"><i class="fab fa-vimeo-v"></i></a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="container-fluid copyright-section">
        <p>Copyright <a href="#">Â© CODE4EDUCATION.</a> All Rights Reserved</p>
    </div>
</section>
<!-- Footer section exit -->









<!-- Bootstrap 5 JS CDN Links -->
<script src="js/popper.min.js"></script>
<script src="js/bootstrap.min.js"></script>

<script src="js/swiper-bundle.min.js"></script>

<script src="js/main.js">
</script>
</body>
</html>



```
















