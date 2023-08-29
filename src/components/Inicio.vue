<script>
import Footer from "./Footer.vue"
window.navigator.vibrate(300);
console.log(navigator.connection);
export default{
    name:'Inicio',
    components:{Footer},
    data(){
        return{

        }
    }
}
</script>

<template>
    <div class="inicio lg:pl-48 lg:pr-44">
       <section class="banner h-44 lg:h-48 flex justify-center items-center">
            <h1 class="font-semibold text-xl text-slate-100 bg-slate-700 p-4">Um lugar para guardar todo o <span class="font-bold">Universo</span></h1>
       </section>
       <!-- flash -->
       <section class="flex flex-wrap  gap-6 lg:gap-8 justify-center items-center py-10">
            <div class="">
                <img src="../assets/img/op1.png" alt="terra" class="w-10 md:w-20 lg:w-20">
                
            </div>
            <div class="">
                <img src="../assets/img/op2.png" alt="terra" class="w-10 md:w-20 lg:w-20">
                
            </div>
            <div class="">
                <img src="../assets/img/op5.png" alt="terra" class="w-10 md:w-20 lg:w-20">
                
            </div>
            <div class="">
                <img src="../assets/img/op4.png" alt="terra" class="w-10 md:w-20 lg:w-20">
                
            </div>
       </section>
       <!--  -->
       <div>
            <div class="text-center mt-10">
                <RouterLink to="/planetas" class="p-3 underline text-slate-600 font-bold text-xl lg:2xl">Venha Descobrir</RouterLink>
            </div>
       </div>
    </div>
    <Footer />
</template>

<style scoped>
    .banner{
        background-image: url("../assets/img/fundo2.png");
        background-repeat: none;
        background-size: cover;
        background-position:left;
    }
</style>