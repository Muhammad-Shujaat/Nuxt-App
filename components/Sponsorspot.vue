<template>
    <div class="w-full" v-if="img">
        <img :src="`/img/${img}`" alt="" class="w-full">

    </div>
</template>
<script setup>
    defineProps({
        img:String
    })
</script>