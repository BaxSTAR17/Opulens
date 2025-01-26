<script setup lang="ts" defer>
    /*const items = [
        'https://picsum.photos/1920/1080?random=1',
        'https://picsum.photos/1920/1080?random=2',
        'https://picsum.photos/1920/1080?random=3',
        'https://picsum.photos/1920/1080?random=4',
        'https://picsum.photos/1920/1080?random=5'
    ]
    const carouselFlip = ref();

    onMounted(() => {
        setInterval(() => {
            if(!carouselFlip) return
            if(carouselFlip.value.page === carouselFlip.value.pages) return carouselFlip.value.select(0)
            carouselFlip.value.next()
        }, 3000)
    })*/
    //let windowWidth = window.innerWidth;
</script>

<template>
    <main class="wrap">
        <div class="navbar">
            <div class="title"></div>
            <div class="menu">
                <a href="" class="nav">ABOUT US</a>
                <a href="" class="nav">EVENTS</a>
                <a href="" class="nav">BOOTHS</a>
                <a href="" class="nav">CONNECT</a>
            </div>
        </div>
        <div class="scene one-carousel">
            <!-- <UCarousel ref="carouselFlip" v-slot="{ item }" :items="items" :ui="{ item: 'basis-full' }" class="maincarousel" indicators>
                <img :src="item" class="carouselpic" draggable="false">
            </UCarousel> -->
            <div class="maincarousel">
                <div class="carouselpic" style="background-image: url('https://picsum.photos/1920/1080?random=1'); --delay: 1"></div>
                <div class="carouselpic" style="background-image: url('https://picsum.photos/1920/1080?random=2'); --delay: 2"></div>
                <div class="carouselpic" style="background-image: url('https://picsum.photos/1920/1080?random=3'); --delay: 3"></div>
                <div class="carouselpic" style="background-image: url('https://picsum.photos/1920/1080?random=4'); --delay: 4"></div>
                <div class="carouselpic" style="background-image: url('https://picsum.photos/1920/1080?random=5'); --delay: 5"></div>
                <div class="carouselpic" style="background-image: url('https://picsum.photos/1920/1080?random=6'); --delay: 6"></div>
                <div class="header">OPULENS</div>
                <div class="subtext">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates eos quia quibusdam</div>
            </div>
        </div>
        <div class="scene two-about">
            <div class="about-container">
                <div class="about-desc">
                    <div class="about-header">Brief Desc</div>
                    <div class="about-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit enim, delectus mollitia fugiat aliquid aliquam sapiente minima animi, eaque natus modi neque labore ducimus.</div>
                    <div class="about-btn">LEARN MORE</div>
                </div>
                <div class="about-pic"></div>
            </div>
        </div>
        <div class="header" style="background-color: white; color: black; text-align: center;" v-motion-pop-visible>SAMPLE SHOTS</div>
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