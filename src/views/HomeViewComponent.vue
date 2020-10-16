<template>
    <v-main>
        <SeriesComponent />
        <CategoriesComponent />
    </v-main>
</template>

<script>
    import SeriesComponent from "../components/SeriesComponent/SeriesComponent";
    import CategoriesComponent from "../components/CategoriesComponent/CategoriesComponent";
    export default {
        name: "HomeViewComponent",
        components: {
            SeriesComponent,
            CategoriesComponent
        },
    }
</script>