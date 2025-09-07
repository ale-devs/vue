<template>
    <div>
        <div class="flex flex-col justify-between gap-4 border border-gray-100 rounded-lg p-5 shadow w-96">
            <div class="border-b border-gray-200 flex justify-center">
                <img class="w-56 h-38" :src="image" alt="title">
            </div>
            <h1 class="text-center font-semibold text-gray-500">{{title}}</h1>
            <a class="border border-[#95D4F5] rounded-lg text-center text-gray-600 py-1" :href="url" target="_blank">{{nameButton}}</a>
        </div>
    </div>
</template>

<script>

    export default{
        name: 'cardsN',
        props: {
            image:String,
            title:String,
            url:String,
            nameButton:String
        }
    }
</script>