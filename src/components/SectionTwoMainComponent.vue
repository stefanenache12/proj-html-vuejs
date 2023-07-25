<script>
    export default {
        name: "SectionTwoMainComponent",
        data() {
            return {
                columnsData: [
                    {
                        title: 'Trim & Cut',
                        image: 'src/barber-shop/img/avadabarbers-trimcut-icon-before.png',
                        content: 'Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiculously good looking.'
                    },
                    {
                        title: 'Wash & Dry',
                        image: 'src/barber-shop/img/avadabarbers-washndry-icon.png',
                        content: 'Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion.'
                    },
                    {
                        title: 'Beard Tidy',
                        image: 'src/barber-shop/img/avadabarbers-beardtrim-icon.png',
                        content: 'Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.'
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
            <div>
                <h6>
                    MENS GROOMING
                </h6>
                <h2>
                    Services
                </h2>
            </div>
            <div class="row">
                <div class="col-4 p-5" v-for="column in columnsData">
                    <img :src="column.image" :alt="column.title">
                    <h4>{{ column.title }}</h4>
                    <p>{{ column.content }}</p>
                </div>
            </div>
            <button>READ ABOUT OUR SERVICES</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *; 

    section {
        width: 100%;
        padding-bottom: 100px;
        position: relative;

        .section-container {
            width: 70%;
            margin: auto;
            padding: 20px 0;

            h6 {
                color: $primary-color;
                font-family: $second-font;
                font-weight: 600;
                letter-spacing: 3px;
            }

            h2 {
                color: $second-color;
                font-family: $primary-font;
                font-size: 3.5rem;
                padding-bottom: 2.5rem;
            }

            button {
                @include buttonPrimary;
                margin: 40px 0 80px 0;
                padding: 15px 50px;
            }
            .row {
                img {
                    max-width: 90px;
                    max-height: 110px;
                    
                }

                h4 {
                    padding: 20px 0;
                    font-family: $primary-font;
                    color: $primary-color;
                    font-size: 1.8rem;
                }

                p {
                    font-family: $second-font;
                    line-height: 1.5;
                }
            }
            
        }
        &::after {
            content: ""; 
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 100px;
            background-image: url('src/barber-shop/img/triangle.svg');
            background-size: cover;
            filter: brightness(7.5%);
        }
    }
</style>