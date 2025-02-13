<script setup lang="ts" defer>
    const items = [
        '/photos/soon.png',
        '/photos/soon.png',
        '/photos/soon.png',
        '/photos/soon.png'
    ]
</script>

<template>
    <main class="wrap">
        <NavBar></NavBar>
        <div class="clip calendar"></div>
        <div class="clip semi carousel">
            <div class="phot" style="--num: 1"></div>
            <div class="phot" style="--num: 2"></div>
            <div class="phot" style="--num: 3"></div>
            <div class="phot" style="--num: 4"></div>
            <div class="phot" style="--num: 5"></div>
            <div class="phot" style="--num: 6"></div>
            <div class="phot" style="--num: 7"></div>
            <div class="phot" style="--num: 8"></div>
            <div class="phot" style="--num: 9"></div>
        </div>
        <div class="clip captured">
            <div class="events">
                <div class="events-title">EVENTS CAPTURED</div>
                <UCarousel
                v-slot="{ item }"
                :items="items"
                :ui="{
                    item: 'basis-full md:basis-1/2 lg:basis-1/3 justify-center',
                }"
                :prev-button="{
                    color: 'white',
                    icon: 'i-mdi-light-chevron-left',
                    size: 'xl'
                }"
                :next-button="{
                    color: 'white',
                    icon: 'i-mdi-light-chevron-right',
                    size: 'xl'
                }"
                arrows
                class="events-slider">
                    <img :src="item" alt="picture" class="slides" draggable="false">
                </UCarousel>
            </div>
        </div>
    </main>
</template>
<style>@import '../public/events.css';</style>