<template>
  <section>
      <img src="../store/park.jpg" alt="">
      <div class="name"> <div class="left">{{name}} {{surname}} </div><div class="right">{{clanska}}</div></div>
      
  </section>
</template>

<script>
export default {
 data(){
   return{
     name:this.$route.query.name,
     surname:this.$route.query.surname,
     clanska:this.$route.query.clanska
   }
 },

}
</script>

<style scoped>
section{
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  height: 30rem;
  width: 40rem;
  top: 50%;
  left: 50%;
  position: absolute;
  transform: translate(-50%,-50%);
  display: grid;
  grid-template-rows:13rem 5.5rem 11.5rem;
  grid-template-columns:3.5rem 13.5rem 23rem;
}
  img{
    height: 100%;
    grid-row: 1/-1;
    grid-column: 1/-1;

  }

  .name{
    position: absolute;
    top: 35%;
    left: 1%;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1.5rem;
    width: 100%;
    height: 2rem;
    transform: perspective(10rem) rotateY(20deg) rotate(-1deg);
    transform-origin: left;
    font-weight: 600;
    
    grid-column: 2/3;
    grid-row: 2/3;
    text-transform:uppercase;
    z-index: 1;
    white-space: nowrap;
    color: white;
    display: flex;
    justify-content: space-between;
  }


    .right{
        position: absolute;
        left:  155%;
    }


</style>