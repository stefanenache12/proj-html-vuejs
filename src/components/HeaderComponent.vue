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
                ]
            }
        },
        methods: {}
    }
</script>

<template>
    <header>
        <div class="header-container">

            <nav>
                <div class="row align-items-center">
                    <div class="col-11">
                        <img :src="images.logo" alt="Barber Logo">
                    </div>
                    <div class="col">
                        <i class="fa-solid fa-cart-shopping fa-2x"></i>
                    </div>
                    <div class="col">
                        <i class="fa-solid fa-bars fa-2x"></i>
                    </div>
                </div>
            </nav>

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
    
    header {
        width: 100%;
        height: 100vh;
        background-image: url('src/barber-shop/img/avadabarbers-homepage-hero-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        color: white;
        position: relative;

        .header-container {
            width: 75%;
            margin: 0 auto;

            nav {
                padding: 40px 0;

                .row {
                    flex-wrap: nowrap;
                }

                img {
                    max-width: 200px;
                }

                .fa-2x {
                    font-size: 25px;
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
                    padding-top: 100px;
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
                    background-color: transparent;
                    color: $primary-color;
                    border: 2px solid $primary-color;
                    padding: 15px 40px;
                    font-size: 1.2rem;
                    transition: all ease;
                }

                button:hover{
                    opacity: 0.8;
                }
            }
        }
    }

</style>