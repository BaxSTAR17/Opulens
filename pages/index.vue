<script setup lang="ts" defer>
    const navs = [
        [
            {label: 'About Us'},
            {label: 'Events'},
            {label: 'Booths'},
            {label: 'Connect with us!'},
        ]
    ]
</script>

<template>
    <main class="wrap">
        <div class="navbar">
            <div class="title"></div>
            <div class="menu">
                <a href="" class="nav">About Us</a>
                <a href="" class="nav">Events</a>
                <a href="" class="nav">Booths</a>
                <a href="" class="nav">Connect with us!</a>
            </div>
            <UDropdown class="dropdown" :items="navs" :popper="{ placement: 'bottom-end' }" :ui="{ background: 'bg-gray-200 dark:bg-gray-300', padding: '0' }">
                <UButton class="navdrop" trailing-icon="i-uil-bars" color="gray"/>

                <template #item="{ item }">
                    <a href="" class="nav">{{ item.label }}</a>
                </template>
            </UDropdown>
        </div>
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
        <div class="header" style="background-color: white; color: black; text-align: center;">SAMPLE SHOTS</div>
        <div class="scene semi samples">
            <div class="samp" style="--delay: 1; background-image: url('https://picsum.photos/1920/1080?random=6');"></div>
            <div class="samp" style="--delay: 2; background-image: url('https://picsum.photos/1920/1080?random=7');"></div>
            <div class="samp" style="--delay: 3; background-image: url('https://picsum.photos/1920/1080?random=8');"></div>
            <div class="samp" style="--delay: 4; background-image: url('https://picsum.photos/1920/1080?random=9');"></div>
            <div class="samp" style="--delay: 5; background-image: url('https://picsum.photos/1920/1080?random=10');"></div>
            <div class="samp" style="--delay: 6; background-image: url('https://picsum.photos/1920/1080?random=11');"></div>
            <div class="samp" style="--delay: 7; background-image: url('https://picsum.photos/1920/1080?random=12');"></div>
            <div class="samp" style="--delay: 8; background-image: url('https://picsum.photos/1920/1080?random=13');"></div>
        </div>
    </main>
</template>

<style>@import '../public/styler.css';</style>