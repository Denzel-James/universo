<script>
    import axios from 'axios'
    import Footer from "./Footer.vue"
export default{
    name:'Planetas',
    components:{Footer},
    data(){
        return{
            dados:null,
            info:null
        }
    },
    mounted(){
        axios.get('https://api.nasa.gov/planetary/apod?api_key=pfufuhoeLhHEmbBX4ieEeCLX10iIoScrffh5odsd&start_date=2017-05-08&end_date=2017-05-20').then((response) => {
        this.dados=response.data;
        console.log(this.dados)
      })
    }
}
</script>
<template>
    <div class="flex flex-wrap lg:gap-4 justify-center mt-10">
        <div class="md:w-1/2 lg:w-1/5 border-2" v-for="(dado, index) in dados">
            <img :src="dado.url" class=" w-full">
            <div class="m-2">
                <p class="font-semibold text-xl text-purple-600">{{ dado.title }}</p>
                <router-link :to="{ name: 'planeta', params: { id:index } }">
                    Ler mais 2
                </router-link>
                <!-- <RouterLink to="/planeta?idDados=dado.title" class="hover:underline hover:font-
                semibold">Saber mais</RouterLink> -->

            </div>
        </div>
    </div>
    <Footer />
</template>