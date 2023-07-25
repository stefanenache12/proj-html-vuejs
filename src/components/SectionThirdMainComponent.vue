<script>
    export default {
        name: "SectionThirdMainComponent",
        data() {
            return {
                columnsData:[
                    {
                        image:'src/barber-shop/img/brush_dark.png',
                        name: 'Brush',
                        price: '$15.00'
                    },
                    {
                        image:'src/barber-shop/img/scissors.png',
                        name: 'Scissors',
                        price: '$85.00'
                    },
                    {
                        image:'src/barber-shop/img/hot_oil_dark.png',
                        name: 'Hot Oil',
                        price: '$15.00' 
                    },
                    {
                        image:'src/barber-shop/img/straight_razor_dark.png',
                        name: 'Straight Razor',
                        price: '$30.00'
                    }
                ]
            }
        },
        methods: {}
    }
</script>

<template>
    <section>
        <div class="section-container text-center">
            <h6>WE HAVE YOU COVERED</h6>
            <h2>Avada Grooming Products</h2>
            <div class="row">
                <div class="col-3" v-for="column in columnsData">
                    <img :src="column.image" :alt="column.name">
                    <h4>{{ column.name }}</h4>
                    <h6>{{ column.price }}</h6>
                </div>
            </div>
            <button>SHOP OUR PRODUCT RANGE</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;

    section {
        background-image: url('src/barber-shop/img/avadabarbers-reviewsbackground.jpg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 800px;

        .section-container {
            width: 80%;
            margin: auto;
            padding: 50px 0;

            h6 {
                font-family: $second-font;
                color: $primary-color;
            }

            h2 {
                font-family: $primary-font;
                color: $second-color;
                font-size: 3.5rem;
                padding: 20px 0 80px 0;
            }

            .row {
                img {
                    width: 100%;
                    scale: 1.3;
                    transition: all 0.3s ease;
                    cursor: pointer;

                    &:hover{
                        scale: 1.5;
                    }
                }

                h4 {
                    color: $primary-color;
                    font-family: $primary-font;
                    padding: 30px 0 5px 0;
                }
            }

            button {
                @include buttonPrimary;
                padding: 15px 60px;
                margin-top: 50px;
            }
        }
    }
</style>