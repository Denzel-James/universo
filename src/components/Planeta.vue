<script>
import axios from 'axios'

    export default{
        name:'Planeta',
        props:['id'],
        data(){
            return{
                card:null,
                index:null
            }
        },
        async mounted(){
            try {

            axios.get('https://api.nasa.gov/planetary/apod?api_key=pfufuhoeLhHEmbBX4ieEeCLX10iIoScrffh5odsd&start_date=2017-05-08&end_date=2017-05-20').then((response) => {

                this.index = this.$route.params.id;
                this.card=response.data[this.index];
                //console.log(this.card)
                console.log(this.index)
            })
            console.log(this.card);
            } catch (error) {
                console.error('Erro ao carregar detalhes do card:', error);
                }
        }
    }
</script>

<template>
    <div class="lg:w-1/3 mx-auto mt-5">
        <RouterLink to="/planetas" class="font-semibold border-2 p-1">Voltar</RouterLink>
        <div class="div py-10">
            <div v-if="card">
                <p class="pb-2">Editor: Denzel James - {{card.date}}</p>
                <img :src="card.url" alt="" class="lg:w-1/1">
                <p class="font-bold text-xl lg:text-2xl pt-5 pb-2">{{card.title}}</p>
                <p>{{card.explanation}}</p>
            </div>
        </div>
    </div>
</template>