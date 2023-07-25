<script>
    
    export default {
        name: "HeaderComponent",
        data() {
            return {
                images: {
                    logo: 'src/barber-shop/img/avadabarbers-logo-x2.png',
                    sectionOneHero:'src/barber-shop/img/avadabarbers_hero_focalmirror-800x1100.png'
                },
                menu: [
                    'Home',
                    'About Us',
                    'Services',
                    'Shop',
                    'Our Team',
                    'Blog',
                    'Contact Us'
                ],
                isScrolled: false,
            }
        },
        methods: {
            handleScroll() {
                const scrollPosition = window.scrollY;
                this.isScrolled = scrollPosition > 0;
            }
        },
        mounted() {
            window.addEventListener('scroll', this.handleScroll);
        },
        beforeDestroy() {
            window.removeEventListener('scroll', this.handleScroll);
        }
    }
</script>

<template>
    <header>
        <div class="header-container">
            <div :class="['nav-container fixed-top', { 'scrolled': isScrolled }]">
                <nav>
                    <div class="row align-items-center">
                        <div class="col-11">
                            <img :src="images.logo" alt="Barber Logo">
                        </div>
                        <div class="col text-end">
                            <button>
                                <i class="fa-solid fa-cart-shopping fa-2x"></i>
                            </button>
                        </div>
                        <div class="col text-end">
                            <button type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasTop" aria-controls="offcanvasTop">
                                <i class="fa-solid fa-bars fa-2x"></i>
                            </button>
                            <div class="offcanvas offcanvas-top" tabindex="-1" id="offcanvasTop" aria-labelledby="offcanvasTopLabel">
                                <div class="offcanvas-header">
                                    <h5 class="offcanvas-title" id="offcanvasTopLabel"></h5>
                                    <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"> <i class="fa-solid fa-xmark fa-2x"></i> </button>
                                </div>
                                <div class="offcanvas-body">
                                    <ul>
                                        <li v-for="menuItem in menu">
                                            <a href="#"> {{ menuItem }} </a>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </nav>
            </div>
            <div class="hero-section">
                <div class="row">
                    <div class="col-6">
                        <h1>
                            Barber Shop
                        </h1>
                        <p>
                            The Pinnacle of Male Grooming
                        </p>
                        <button>
                            LEARN MORE
                        </button>
                    </div>
                    <div class="col">
                        <img :src="images.sectionOneHero" alt="Hero Image">
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;  
    
    header {
        width: 100%;
        height: 100vh;
        background-image: url('src/barber-shop/img/avadabarbers-homepage-hero-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        
        color: white;
        position: relative;
        overflow-y: hidden;
        .header-container {
            width: 75%;
            margin: 0 auto;
            .nav-container {
                width: 100%;
                height: max-content;
                background-color: transparent;
                transition: all 0.3s ease;
                padding: 40px 0;
                overflow-y: hidden;
                &.scrolled {
                background-color: black;
                padding: 5px 0;
                }

                nav {
                width: 75%;
                margin: 0 auto;
                .row {
                    flex-wrap: nowrap;
                }

                img {
                    max-width: 200px;
                }

                .fa-2x {
                    font-size: 25px;
                }

                button {
                    background-color: transparent;
                    border: none;
                    color: white;
                    padding: 2px;
                }

                button:hover {
                    color: $primary-color;
                }

                ul {
                    list-style: none;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    padding: 20px 0;

                    li {
                        padding: 20px;
                        font-family: $second-font;
                        font-weight: 600;
                        font-size: 1.5rem;
                        cursor: pointer;
                        width: fit-content;

                        a {
                            text-decoration: none;
                            color: white;
                        }
                    }

                    a:hover {
                        color: $primary-color;
                    }
                }
            }
            }
            
            .hero-section{

                img {
                    max-width: 500px;
                    position: absolute;
                    top: 3.125rem;
                }

                h1 {
                    font-family: $primary-font;
                    font-size: 5.5rem;
                    padding-top: 250px;
                    padding-bottom: 25px;
                    position: relative;

                }

                h1:before {
                    content: ""; 
                    position: absolute;
                    bottom: 0;
                    width: 50%; 
                    border-bottom: 4px solid $primary-color;
                }

                p {
                    font-family: $second-font;
                    font-size: 1.5rem;
                    color: $second-color;
                    padding: 25px 0;
                }

                button {
                    @include buttonPrimary;
                }
            }

            .offcanvas {
                --bs-offcanvas-height: 100vh;
                --bs-offcanvas-color: white;
                --bs-offcanvas-bg: rgba(0, 0, 0, );
                .btn-close {
                    --bs-btn-close-color: white;
                    --bs-btn-close-bg: none;
                }
            }
        }
    }

</style>