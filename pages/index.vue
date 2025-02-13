<script setup lang="ts" defer>
    const items = [
        '/photos/soon.png',
        '/photos/soon.png',
        '/photos/soon.png'
    ]
</script>

<template>
    <main class="wrap">
        <NavBar></NavBar>
        <div class="scene one-carousel">   
            <div class="header"></div>
            <div class="presser">WORK WITH ME!</div>
        </div>
        <div class="scene two-about">
            <div class="about-container">
                <div class="about-desc">
                    <div class="about-header">OPULENS</div>
                    <div class="about-text">Our photobooth isn’t just about taking pictures—it’s about bringing people together. Whether it’s a wedding, birthday, corporate event, or any special occasion, our photobooth creates a fun and seamless way to capture shared joy and laughter. Photos have a unique ability to unite generations, spark connections, and make moments truly timeless.
                    <br><br>
                    At OPULENS, we’re dedicated to turning moments into memories, and memories into forever. Let us help you celebrate life’s precious moments and make them truly unforgettable!</div>
                    <button class="presser about-btn">LEARN MORE</button>
                </div>
                <div class="about-pic"></div>
            </div>
        </div>
        <div class="scene samples">
            <div class="samples-title">FEATURED</div>
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
                <img :src="item" alt="picture" class="pics" draggable="false">
            </UCarousel>
        </div>
    </main>
</template>

<style>@import '../public/styler.css';</style>