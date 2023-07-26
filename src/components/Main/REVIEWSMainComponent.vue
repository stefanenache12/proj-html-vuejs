<script>
    export default {
        name: "REVIEWSMainComponent",
        data() {
            return {
                reviews: [
                    {
                        text:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.',
                        image:'src/barber-shop/img/avadabarbers-trimcut-gallery6.jpg',
                        name:'John Doe'
                    },
                    {
                        text:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.',
                        image:'src/barber-shop/img/avadabarbers-trimcut-gallery7.jpg',
                        name:'Pete Jones'
                    },
                    {
                        text:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.',
                        image:'src/barber-shop/img/avadabarbers-trimcut-gallery3.jpg',
                        name:'Mark Wilson'
                    },
                ]
            }
        },
        methods: {}
    }
</script>

<template>
    <section>
        <div class="section-container text-center">
            <h6>
                WHAT PEOPLE SAY
            </h6>
            <h2>
                Reviews
            </h2>
            <div class="row ">
                <div class="col-4" v-for="review in reviews">
                    <p>
                        {{ review.text }}
                    </p>
                    <div class="img-container">
                        <img :src="review.image" :alt="review.name">
                    </div>
                    <h6>
                        {{ review.name }}
                    </h6>
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
        .section-container {
            width: 80%;
            margin: auto;

            h6 {
                color: $primary-color;
                font-family: $second-font;
                letter-spacing: 2px;
            }

            h2 {
                font-family: $primary-font;
                color: $second-color;
                font-size: 4rem;
                padding: 10px 0 30px 0;
            }
            .col-4 {
                padding: 0 5rem;
                .img-container {
                    width: 120px;
                    display: inline-block;
                    
                    img {
                        width: 100%;
                        border-radius: 50%;
                        margin-bottom: 20px;
                    }
                }

                p {
                    color: #686868;
                    margin-bottom: 20px;
                    font-family: $second-font;
                }
            }
        }

        &:before {
            content: ""; 
            position: absolute;
            bottom: -100px;
            width: 100%;
            height: 100px;
            background-image: url('src/barber-shop/img/triangle.svg');
            background-size: cover;
            background-color: #F5F5F5;
            transform: rotate(180deg);
        }
    }
</style>