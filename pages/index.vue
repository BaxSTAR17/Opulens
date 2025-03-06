<script setup lang="ts" defer>
    const items = [
        {
            src: '/photos/ValentinesBazaar.jfif',
            event_name: "The Henry's Resort Pre-Valentines Bazaar (LAUNCH DAY)",
            event_date: 'February 12-13, 2025'
        },
        {
            src: '/photos/ValentinesSU.jfif',
            event_name: "Silliman Valentines Pop-Up Bazaar",
            event_date: 'February 14, 2025'
        },
        {
            src: '/photos/Bahia.jfif',
            event_name: "BAHIA The Inner Circle x Jäegermeister’s Valentines Party",
            event_date: 'February 14, 2025'
        },
        {
            src: '/photos/LACEDpopup.jfif',
            event_name: "Laced Pop-Up Bazaar",
            event_date: 'February 22, 2025'
        },
        {
            src: '/photos/lacedparty.jfif',
            event_name: "Laced Valentine's Party",
            event_date: 'February 22, 2025'
        }
    ];
</script>

<template>
    <main class="wrap">
        <NavBar></NavBar>
        <div class="scene one-carousel">   
            <div class="header"></div>
            <div class="presser">WORK WITH ME!</div>
        </div>
        <div class="scene two-about" id="about">
            <div class="about-container">
                <div class="about-desc">
                    <div class="about-header">OPULENS</div>
                    <div class="about-text">Our photobooth isn’t just about taking pictures—it’s about bringing people together. Whether it’s a wedding, birthday, corporate event, or any special occasion, our photobooth creates a fun and seamless way to capture shared joy and laughter. Photos have a unique ability to unite generations, spark connections, and make moments truly timeless.
                    <br><br>
                    At OPULENS, we’re dedicated to turning moments into memories, and memories into forever. Let us help you celebrate life’s precious moments and make them truly unforgettable!</div>
                    <button class="presser about-btn" onclick="">LEARN MORE</button>
                </div>
                <div class="about-pic"></div>
            </div>
        </div>
        <div class="scene samples">
            <UCarousel
            v-slot="{ item }"
            :items="items"
            :ui="{
                item: 'basis-full',
                container: 'rounded-md'
            }"
            :prev-button="{
                color: 'black',
                icon: 'i-mdi-light-arrow-left'
            }"
            :next-button="{
                color: 'black',
                icon: 'i-mdi-light-arrow-right'
            }"
            arrows
            class="samp">
                <img :src="item.src" alt="picture" class="pics" draggable="false">
                <div class="event">
                    <div class="name">{{ item.event_name }}</div>
                    <span class="date">{{ item.event_date }}</span>
                </div>
            </UCarousel>
        </div>
    </main>
</template>

<style>@import '../public/styler.css';</style>