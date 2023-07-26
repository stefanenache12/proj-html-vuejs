<script>
    export default {
        name: "FooterComponent",
        data() {
            return {}
        },
        methods: {}
    }
</script>

<template>
    <footer>
        <section class="section-top">
            <div class="section-top-container">
                <div class="row">
                    <div class="col-4">
                        <div>
                            <img src="src/barber-shop/img/avadabarbers_footer_shop_image-600x468.png" alt="">
                        </div>
                        <button>SHOP OUR RANGE NOW</button>
                    </div>
                    <div class="col-4">
                        <div class="logo">
                            <img src="src/barber-shop/img/avadabarbers-logo-x2-300x104.png" alt="LOGO">
                        </div>
                        <p>
                            Avada Barbers
                            <br>
                            123 New York Street
                            <br>
                            New York City
                            <br>
                            info@yourwebsite.com
                            <br>
                            +1 (555) 555-1212
                        </p>
                        <h6>
                            FOLLOW US
                        </h6>
                        <div>
                            <a href="#">
                                <i class="fa-brands fa-facebook-f"></i>
                            </a>
                            <a href="#">
                                <i class="fa-brands fa-twitter"></i>
                            </a>
                            <a href="#">
                                <i class="fa-brands fa-instagram"></i>
                            </a>
                            <a href="#">
                                <i class="fa-brands fa-youtube"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-4">
                        <div>
                            <img src="src/barber-shop/img/avadabarbers_footer_appointment_image-600x468.png" alt="">
                        </div>
                        <button>BOOK YOUR APPOINTMENT</button>
                    </div>
                </div>
            </div>
        </section>
        <section class="section-bottom">
            <div class="section-bottom-container">
                <p>
                    © Copyright 2023 | Made by Stefan Enache | All Rights Reserved | Powered by Boolean
                </p>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *; 

    footer {
        width: 100%;

        .section-top {
            width: 100%;
            background-color: #121314;
            padding: 80px 0;

            .section-top-container {
                width: 75%;
                margin: auto;
                text-align: center;

                .logo img {
                    max-width: 200px;
                    padding-bottom: 40px;
                    transition: all 0.5s ease;
                    cursor: pointer;

                    &:hover{
                        scale: 1.2;
                    }
                }

                p {
                    color: #686868;
                    font-family: $second-font;
                }

                h6 {
                    font-family: $second-font;
                    color: $primary-color;
                    padding-top: 50px;
                    padding-bottom: 30px;
                }

                a {
                    color: #686868;
                    margin: 0 10px;
                }

                img {
                    max-width: 350px;
                }

                button {
                    @include buttonPrimary;
                    margin-top: 10px;
                    padding: 10px 40px;
                }
            }
        }

        .section-bottom {
            width: 100%;
            background-color: #1b1b1b;
            text-align: center;
            color: #686868;
            padding: 40px 0;
        }
    }
</style>