<template>
    <div class="flex gap-5 p-5">
        <div class="w-62">
            <Aside/>
        </div>
        <div class="w-full mt-20">
            <div class="fixed top-0 left-60 bottom-220 w-full shadow px-2">
                <h1 class="text-2xl font-bold text-red-900 bg-white">{{ title }}</h1>
                <h2 class="text-lg font-bold text-gray-400 bg-white">Plataforma estudiantil</h2>
            </div>
            <div>
                <h1 class="text-xl font-semibold text-red-800 mb-5">Contenido disponible</h1>
                <div class="flex flex-col items-center w-full">
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <Card v-for="(card) in cards" :key="card.card" :image="card.image" :title="card.title" :url="card.url" :nameButton="card.nameButton"/>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>
<script>
import Aside from "./Aside.vue";
import Card from "./Card.vue";
import jsImage from '../assets/js-image.jpg';
import vueImage from '../assets/vue-image.jpg';
import htmlImage from '../assets/html-image.jpg';

    export default {
        name: 'encabezadoM',
        data(){
            return {
                cards: [
                    {
                        card: 1,
                        image: jsImage,
                        title:"Curso disponible de Js",
                        url:"https://www.itca.edu.sv/",
                        nameButton:"Más informacion"
                    },
                    {
                        card: 2,
                        image:vueImage,
                        title:"Curso disponible de Vue",
                        url:"https://www.itca.edu.sv/",
                        nameButton:"Más informacion"
                    },
                    {
                        card: 3,
                        image:htmlImage,
                        title:"Curso disponible de Html",
                        url:"https://www.itca.edu.sv/",
                        nameButton:"Más informacion"
                    }
                ]
            }
        },
        props: {
            title: String
        },
        components: {
            Aside,
            Card
        }
    }
</script>