<template>
    <div class="row p-5">
        <div class="w-full flex flex-col-reverse md:grid grid-cols-3 gap-10">
            <div class="w-full md:col-span-2 grid md:grid-cols-2 gap-5">
                <!-- big card -->
                <div class="w-full col-span-full">
                    <ArticleCard img="big-card.png" title="EN LASER FORTALLER"
                        text="Jeg higede efter omsorg - del 2:5" />
                </div>
                <!-- small cards  -->

                <ArticleCard v-for="(card, i) in cards" :key="i" :img="card.img" :text="card.text"
                    :title="card.title" />
            </div>
            <!-- sponsor card  -->
            <div class="w-full">
                <Sponsorspot img="sponsor.png" />
            </div>
        </div>
    </div>
</template>
<script setup>
import Sponsorspot from '~/components/Sponsorspot.vue';

const cards = ref([
    {
        img: "small-card1.png",
        title: "NAR LIVET GOR ONDT",
        text: "33-ärige Dagmar har maske kun fa maneder tilbage",
    },
    {
        img: "small-card2.png",
        title: "NAR LIVET GOR ONDT",
        text: "Stinne og Christian er uhelbredeligt syge med kraft",
    },
]);
</script>