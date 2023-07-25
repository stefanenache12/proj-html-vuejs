<script>
    import SectioneOneMainComponent from './SectioneOneMainComponent.vue';
    import SectionTwoMainComponent from './SectionTwoMainComponent.vue';

    export default {
        name: "MainComponent",
        data() {
            return {}
        },
        methods: {},
        components: {
            SectioneOneMainComponent,
            SectionTwoMainComponent,
        }
    }
</script>

<template>
    <main>
        <SectioneOneMainComponent/>
        <SectionTwoMainComponent/>
    </main>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;

    main {
        width: 100%;
    }
</style>