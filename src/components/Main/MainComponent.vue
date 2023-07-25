<script>
    import AWARDMainComponent from './AWARDMainComponent.vue';
    import SERVICESMainComponent from './SERVICESMainComponent.vue';
    import SHOPMainComponent from './SHOPMainComponent.vue';
    import FEATUREDPRODUCTMainComponent from './FEATUREDPRODUCTMainComponent.vue';
    import REVIEWSMainComponent from './REVIEWSMainComponent.vue';

    export default {
        name: "MainComponent",
        data() {
            return {}
        },
        methods: {},
        components: {
            AWARDMainComponent,
            SERVICESMainComponent,
            SHOPMainComponent,
            FEATUREDPRODUCTMainComponent,
            REVIEWSMainComponent,
        }
    }
</script>

<template>
    <main>
        <AWARDMainComponent/>
        <SERVICESMainComponent/>
        <SHOPMainComponent/>
        <FEATUREDPRODUCTMainComponent/>
        <REVIEWSMainComponent/>
    </main>
</template>

<style lang="scss" scoped>
    @use"src/assets/scss/partials/variables" as *;
    @use"src/assets/scss/partials/mixins" as *;

    main {
        width: 100%;
    }
</style>