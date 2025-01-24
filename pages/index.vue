<script setup lang="ts" defer>
    const items = [
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
    })
</script>

<template>
    <main class="wrap">
        <div class="navbar">
            <div class="title"></div>
            <div class="menu">
                <a href="" class="nav">ABOUT US</a>
                <a href="" class="nav">EVENTS</a>
                <a href="" class="nav">BOOTHS</a>
                <a href="" class="nav">CONTACTS</a>
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
                <div class="header">Sample Text</div>
                <div class="subtext">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates eos quia quibusdam</div>
            </div>
        </div>
        <div class="scene two-about">
            <div class="about-container">
                <div class="about-desc">
                    <div class="about-header"><u>About Opulens</u></div>
                    <div class="about-text">
                        The name "Opulens" is inspired by the word opulence, symbolizing great wealth, abundance, and luxuriousness. Our photobooth embodies this essence by offering a premium, unforgettable experience that adds a touch of elegance and sophistication to every event.
                        <br>
                        <br>
                        We strive to not only bring you a luxurious time but also to create a space where memories are made and cherished forever. With Opulens, every snapshot becomes a moment of joy, connection, and celebration—because life’s precious moments deserve nothing less than the finest.
                    </div>
                </div>
                <div class="aboutpic"></div>
            </div>
        </div>
        <div class="scene three-event">
            <div class="event-container">
                <div class="event-header">
                    EVENTS
                </div>
                <div class="event-scroller">
                    <div class="event-pages"></div>
                    <div class="event-pages"></div>
                    <div class="event-pages"></div>
                </div>
            </div>
        </div>
        <div class="scene four-rates">
            <div class="rates-header">BOOTHS</div>
            <div class="booth-container">
                <div class="booths" style="--cor:-1"></div>
                <div class="booths" style="--cor:1"></div>
                <div class="booths" style="--cor:2"></div>
                <div class="booths" style="--cor:0"></div>
                <div class="booths" style="--cor:-0.5"></div>
                <div class="booths" style="--cor:3"></div>
            </div>
        </div>
        <div class="scene five-contacts">
            <div class="contact-header">CONTACT US!</div>
            <div class="contacters">
                <div class="booths" style="--cor: 1;">
                    <img src="../assets/FontAwesome-Brands-Facebook-icon.png" alt="fb">
                </div>
                <div class="booths" style="--cor: -0.5">
                    <img src="../assets/insta.png" alt="insta" width="250">
                </div>
                <div class="booths" style="--cor: -1">
                    <img src="../assets/email.png" alt="email">
                </div>
            </div>
        </div>
    </main>
</template>

<style>@import '../public/styler.css';</style>