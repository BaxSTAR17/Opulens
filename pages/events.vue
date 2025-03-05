<script setup lang="ts" defer>
    const items = [
        '/photos/eventslaunch.jfif',
        '/photos/eventsvalsu.jfif',
        '/photos/eventsbahia.jfif',
        '/photos/eventslacedpopup.jfif',
        '/photos/eventslacedparty.jfif',
    ]
</script>

<template>
    <main class="wrap">
        <NavBar></NavBar>
        <div class="clip calendar"></div>
        <div class="clip semi carousel">
            <div class="phot" style="--num: 1; background-image: url(./photos/pic1.jfif)"></div>
            <div class="phot" style="--num: 2; background-image: url(./photos/pic2.jfif)"></div>
            <div class="phot" style="--num: 3; background-image: url(./photos/pic3.jfif)"></div>
            <div class="phot" style="--num: 4; background-image: url(./photos/pic4.jfif)"></div>
            <div class="phot" style="--num: 5; background-image: url(./photos/pic5.jfif)"></div>
            <div class="phot" style="--num: 6; background-image: url(./photos/pic6.jfif)"></div>
            <div class="phot" style="--num: 7; background-image: url(./photos/pic7.jfif)"></div>
            <div class="phot" style="--num: 8; background-image: url(./photos/pic8.jfif)"></div>
            <div class="phot" style="--num: 9; background-image: url(./photos/pic9.jfif)"></div>
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