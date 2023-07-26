<script>
    export default {
        name: "BLOGMainComponent",
        data() {
            return {
                blogsData: [
                    {
                        image: 'src/barber-shop/img/avadabarbers-second-blog-700x441.jpg',
                        title: 'Avada Barbers Now Open',
                        content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper.',
                    },
                    {
                        image: 'src/barber-shop/img/avadabarbers-choosing-blog-700x441.jpg',
                        title: 'Choosing The Right Barber',
                        content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper.',
                    },
                    {
                        image: 'src/barber-shop/img/avadabarbers-ourservice-blog-700x441.jpg',
                        title: 'Quick Service Guide of Barbers',
                        content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper.',
                    },
                ]
            }
        },
        methods: {}
    }
</script>

<template>
    <section>
        <div class="section-container">
            <h6>
                TALES FROM THE BARBER SHOP
            </h6>
            <h2>
                Recent Blog Posts
            </h2>
            <div class="row">
                <div class="col-4" v-for="blog in blogsData">
                    <div class="zoom-container">
                        <img :src="blog.image" :alt="blog.title">
                    </div>
                    <h4>
                        {{ blog.title }}
                    </h4>
                    <p>
                        {{ blog.content }}
                    </p>
                </div>
            </div>
            <button>READ MORE FROM OUR BLOG</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *; 

    section {
        padding-top: 100px;
        background-color: #f5f5f5;

        .section-container {
            width: 75%;
            margin: auto;
            text-align: center;

            h6 {
                color: $primary-color;
                letter-spacing: 2px;
                padding-top: 50px;
                font-family: $second-font;
            }

            h2 {
                font-family: $primary-font;
                color: $second-color;
                font-size: 4rem;
                padding-bottom: 40px;
            }

            .row {
                margin: 0 -15px;
            }
            .col-4 {
                padding: 0 15px;
                .zoom-container {
                    overflow: hidden;

                    img {
                        width: 100%;
                        transition: all 1.5s ease;
                        cursor: pointer;

                        &:hover{
                            transform: scale(1.2);
                            filter: blur(0.8px);
                        }
                    }
                }

                h4 {
                    color: $primary-color;
                    font-family: $primary-font;
                    font-size: 2rem;
                    padding: 10px 0;
                }

                p {
                    color: #686868;
                    font-family: $second-font;
                }
            }

            button {
                @include buttonPrimary;
                margin: 50px 0;
            }
        }
    }
</style>