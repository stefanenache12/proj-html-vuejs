<script>
    export default {
        name: "SectionOneMainComponent",
        data() {
            return {}
        },
        methods: {}
    }
</script>

<template>
    <section>
        <div class="section-container">
            <h6>AWARD WINNING</h6>
            <h2>Pro Barbers</h2>
            <button>MEET YOUR NEW BARBER</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *; 

    section {
        width: 100%;
        padding-bottom: 150px;
        background-image: url('src/barber-shop/img/avadabarbers-about-introbackground.jpg');
        background-size: cover;
        position: relative;

        .section-container {
            width: 40%;
            margin: auto;
            text-align: center;
            padding-top: 100px;

            h6 {
                color: $primary-color;
                font-family: $second-font;
            }

            h2 {
                color: $second-color;
                font-family: $primary-font;
                font-size: 4rem;
                padding: .625rem 0 1.25rem 0;
            }

            button {
                @include buttonPrimary;
            }
        }

        &::before {
            content: ""; 
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 100px;
            background-image: url('src/barber-shop/img/triangle.svg');
            background-size: cover;
        }
    }
</style>