<template>
    <section class="first">
        <input type="text" placeholder="Unesi ime" v-model="name"> <br>
        <input type="text" placeholder="Unesi Prezime" v-model="surname"> <br>
        <input type="number" placeholder="Unesi br.clnaske"  maxlength="6"  oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);" v-model="clanska"> <br>
        <button @click="generate">Kreni</button>
    </section>
</template>

<script>
export default {
    data(){
        return{
            name:"",
            surname:"",
            clanska:""
        }
    },
    methods:{
        generate(){
            this.$router.push({ name: 'park', query: { name: this.name, surname:this.surname, clanska:this.clanska } })
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
