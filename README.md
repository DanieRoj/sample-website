# sample-website



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

h3 {
    margin-bottom: 1.875rem;
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

















