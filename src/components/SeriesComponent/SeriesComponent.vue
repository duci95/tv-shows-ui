<template src="./template.html"/>
<style scoped src="./style.css"></style>

<script>
    import ApiService from "../../services/ApiService";

    export default {
        name: "SeriesComponent",
        data: () => ({
            series : []
        }),
        created() {
            this.series = ApiService.apiClient.get('/shows')
                .then(response => {
                    console.log(response.data);
                })
                .catch(_ => {
                });
        }
    }
</script>

