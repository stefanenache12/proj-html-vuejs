<script>
    import SectioneOneMainComponent from './SectioneOneMainComponent.vue';
    import SectionTwoMainComponent from './SectionTwoMainComponent.vue';
    import SectionThirdMainComponent from './SectionThirdMainComponent.vue';

    export default {
        name: "MainComponent",
        data() {
            return {}
        },
        methods: {},
        components: {
            SectioneOneMainComponent,
            SectionTwoMainComponent,
            SectionThirdMainComponent,
        }
    }
</script>

<template>
    <main>
        <SectioneOneMainComponent/>
        <SectionTwoMainComponent/>
        <SectionThirdMainComponent/>
    </main>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;

    main {
        width: 100%;
    }
</style>