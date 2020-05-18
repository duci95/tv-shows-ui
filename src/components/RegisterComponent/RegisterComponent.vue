<template src="./template.html" />

<script>
    import ApiService from "../../services/ApiService";

    export default {
        name: "RegisterComponent",
        data(){
            return {
                showPassword : false,
                firstname:'',
                lastname:'',
                username: '',
                email:'',
                password:'',
                passwordRepeat:''
            }
        },
        methods:{
            async register(){
                await ApiService.apiClient.post('users',{
                    firstname:this.firstname,
                    lastname:this.lastname,
                    username:this.username,
                    email:this.email,
                    password:this.password,
                    passwordRepeat:this.passwordRepeat
                })
                .then(_ =>{
                    alert('Uspeh')
                })
                .catch(_ =>{
                    alert("Nije")
                })
            }
        }
    }
</script>
