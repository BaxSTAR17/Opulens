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
        <div class="scene semi samples">
            
        </div>
        <div class="scene past-work">
            <div class="pastworktitle">
                <span class="pasttitle" v-motion
                :initial="{ opacity: 0, x: -100}"
                :visible="{opacity: 1, x:0}"
                :duration="1300">PAST</span>
                <span class="worktitle" v-motion
                :initial="{ opacity: 0, x: 100}"
                :visible="{opacity: 1, x:0}"
                :delay="1000"
                :duration="1300">Work</span>
            </div>
        </div>
        <div class="scene fashion">
            <div class="fashionheader">
                FASHION FORWARD
                <div class="line"></div>
                <div class="productdesign">Product Design</div>
            </div>
            <div class="fashionbody">
                <div class="fashiondesc">Made designs for Fashion Forward’s accessories using environmental-friendly materials.</div>
                <div class="fashionpic"></div>
            </div>
        </div>
        <div class="scene gordonmm">
            <div class="gordon gheader">
                <span>Multimedia Artist</span>
                <span>Portfolio</span>
            </div>
            <div class="gordon gbody">
                <span class="gordonname">GORDON-</span>
                <span class="gordonlast">Aliprandi</span>
            </div>
            <div class="presser">WORK WITH ME</div>
        </div>
    </main>
</template>

<style>@import '../public/styler.css';</style>