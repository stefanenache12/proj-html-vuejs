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
    return {};
  },
  methods: {},
};
</script>

<template>
    <HeaderComponent/>
    <MainComponent/>
    <FooterComponent/>
</template>

<style lang="scss">
    @use "assets/scss/main";
</style>
