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
            <h4>AWARD WINNING</h4>
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
        height: 450px;
        background-image: url('src/barber-shop/img/avadabarbers-about-introbackground.jpg');
        background-size: cover;
        position: relative;

        .section-container {
            width: 40%;
            margin: auto;
            text-align: center;
            padding-top: 100px;
        }

        &::before {
            content: ""; 
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 130px;
            background-image: url('src/barber-shop/img/triangle.svg');
            background-size: cover;
            
        }
    }

</style>