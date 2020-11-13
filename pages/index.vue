<template>
    <section class="first">
        <input type="text" placeholder="Unesi ime" v-model="name"> <br>
        <input type="text" placeholder="Unesi Prezime" v-model="surname"> <br>
        <button @click="generate" >Kreni</button>
    </section>
</template>

<script>
export default {
    data(){
        return{
            name:"",
            surname:""
        }
    },
    methods:{
        generate(){
            this.$router.push({ name: 'park', query: { name: this.name, surname:this.surname } })
        }
    }
}
</script>

<style>
    .first{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        text-align: center;
    }
    input{
        background-color: beige;
    }
</style>
