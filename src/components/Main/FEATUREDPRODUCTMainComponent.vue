<script>
    export default {
        name: "FEATUREDPRODUCTMainComponent",
        data() {
            return {
                productImage:'src/barber-shop/img/shaving_butter-600x600.png'
            }
        },
        methods: {}
    }
</script>

<template>
    <section>
        <div class="section-container">
            <div class="row text-center">
                <div class="col-5">
                    <img :src="productImage" alt="Shaving Butter">
                </div>
                <div class="col-7 align-self-center text-start">
                    <h6>
                        THIS MONTHS FEATURED PRODUCT
                    </h6>
                    <h2>
                        Shaving Butter
                    </h2>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                    </p>
                    <button>BUY NOW</button>
                </div>
            </div>
        </div>
    </section>    
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;

    section {
        width: 100%;
        position: relative;
        height: min-content;
        padding-bottom: 500px;
        .section-container {
            width: 75%;
            margin: auto;
            background-color: black;
            border-top: 4px solid $primary-color;
            position: absolute;
            top:-50px;
            left: calc(25% / 2);
            .row {
                --bs-gutter-x: 0;
                .col-5 {
                background-image: url('src/barber-shop/img/avadabarbers-cta-background.jpg');
                background-position: center;
                background-size: cover;
                background-repeat: no-repeat;
            
                    img {
                        max-width: 90%;
                    }
                }
                .col-7 {
                    height: fit-content;
                    padding: 0 4.375rem;

                    h6 {
                        color: $primary-color;
                        font-family: $second-font;
                        letter-spacing: 3px;
                    }

                    h2 {
                        color: $second-color;
                        font-family: $primary-font;
                        font-size: 4rem;
                        padding-bottom: .625rem;
                    }

                    p {
                        font-family: $second-font;
                        line-height: 1.8;
                        color: $second-color;
                    }

                    button {
                        @include buttonPrimary;
                        margin-top: .9375rem;
                    }
                }
            }
        }
    }
</style>