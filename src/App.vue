<script>
    import HeaderComponent from './components/Header/HeaderComponent.vue';
    import MainComponent from './components/Main/MainComponent.vue';
    import FooterComponent from './components/Footer/FooterComponent.vue';

    export default {
        name: "App",
        components: {
            HeaderComponent,
            MainComponent,
            FooterComponent,
        },
        data() {
            return {
            showButton: false,
            };
        },
        methods: {
            toggleScrollToTopButton() {
                this.showButton = window.scrollY > 500;
            },
            scrollToTop() {
                window.scrollTo({ top: 0, behavior: 'smooth' });
            },
        },
        mounted() {
            window.addEventListener('scroll', this.toggleScrollToTopButton);
        },
        beforeDestroy() {
            window.removeEventListener('scroll', this.toggleScrollToTopButton);
        }
    };
</script>

<template>
    <HeaderComponent/>
    <MainComponent/>
    <FooterComponent/>
    <div @click="scrollToTop" v-if="showButton" class="scroll-to-top-button">
      <i class="fa-solid fa-square-caret-up fa-3x"></i>
  </div>
</template>

<style lang="scss">
    @use "assets/scss/main";
    @use"src/assets/scss/partials/variables" as *;
    
    .scroll-to-top-button {
        position: fixed;
        bottom: 0;
        right: 20px;
        color: $primary-color;
        cursor: pointer;
    }
</style>
