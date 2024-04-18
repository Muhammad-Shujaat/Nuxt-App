<template>
    <div class="bg-cards w-full flex flex-col items-center overflow-hidden rounded-lg">
        <NuxtImg class="w-full" :src="`/img/${img}`" v-if="img"/>
        <div class="px-10 py-3">
            <p class="text-xs font-bold uppercase text-center text-red" v-if="title">
                {{ title }}
            </p>
            <p class="text-black text-base font-bold w-full max-w-md text-center" v-if="text">{{ text }}</p>
        </div>


    </div>

</template>
<script setup>
defineProps({
    img:String,
    title:String,
    text:String,
})

</script>