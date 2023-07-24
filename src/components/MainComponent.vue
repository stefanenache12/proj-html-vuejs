<script>
    import SectioneOneMainComponent from './SectioneOneMainComponent.vue';

    export default {
        name: "MainComponent",
        data() {
            return {}
        },
        methods: {},
        components: {
            SectioneOneMainComponent,
        }
    }
</script>

<template>
    <main>
        <SectioneOneMainComponent/>
    </main>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;

    main {
        width: 100%;
    }
</style>