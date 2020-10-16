<template src="./template.html"/>
<style scoped src="./style.css"></style>

<script>
    import ApiService from "../../services/ApiService";

    export default {
        name: "SeriesComponent",
        data: () => ({
            series : [],
            totalCount : null,
            totalPages : null,
            pagination:{
                currentPage: 1,
                perPage:5
            },
			perPageSelect : [5,10,15]
        }),
        methods:{
            getSeries(){
                ApiService.apiClient.get('/shows',{
                    params :{
                        pageNumber: this.pagination.currentPage,
						perPage: this.pagination.perPage
					}
				})
                    .then(response => {
                        //treba odraditi pomocu store
                        this.series = response.data.intel;
                        this.totalCount = response.data.totalCount;
                        this.totalPages = response.data.pagesCount;
                    })
                    .catch(_ => {
                    });
            },
            changePage(page){
                this.pagination.currentPage = page;
                this.getSeries();
            }
        },
        created() {
            this.getSeries();
        }
    }
</script>