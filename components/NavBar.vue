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
    <div class="navbar">
        <NuxtLink to="/" class="title"></NuxtLink>
        <div class="menu">
            <NuxtLink to="/" class="nav">About Us</NuxtLink>
            <NuxtLink to="/events" class="nav">Events</NuxtLink>
            <NuxtLink to="" class="nav">Booths</NuxtLink>
            <NuxtLink to="" class="nav">Connect with us!</NuxtLink>
        </div>
        <UDropdown class="dropdown" :items="navs" :popper="{ placement: 'bottom-end' }" :ui="{ background: 'bg-gray-200 dark:bg-gray-300', padding: '0' }">
            <UButton class="navdrop" trailing-icon="i-uil-bars" color="gray"/>

            <template #item="{ item }">
                <a href="" class="nav">{{ item.label }}</a>
            </template>
        </UDropdown>
    </div>
</template>

<style>
    .navbar {
    padding-left: 40px;
    padding-right: 40px;
    box-sizing: border-box;
    width: 100%;
    height: 50px;
    background-color:white;
    display: flex;
    justify-content: space-between;
    } .navbar .title {
        background-image: url(../assets/logo.png);
        width: 90px;
        height: 50px;
        background-size: cover;
        background-position: center center;
        /* border: 1px solid red; */
    } .navbar .menu {
        display: flex;
        width: fit-content;
        height: 50px;
    } .navbar .menu .nav {
        font-family: subtext;
        width: 120px;
        height: 50px;
        border-left: 1px solid white;
        border-right: 1px solid white;
        justify-content: center;
        font-size: 0.9em;
        display: flex;
        align-items: center;
        text-decoration: none;
        color: black;
        transition: all 0.2s ease-in-out;
    } .navbar .menu .nav:hover {
        color: white;
        background-color: black;
        cursor: pointer;
        text-decoration: underline;
    } .navbar .dropdown {display:none; visibility: hidden;}

    @media screen and (max-width: 650px) {
        .navbar .menu .nav, .navbar .menu {
            display: none;
            visibility: hidden;
            width: 0px;
            height: 0px;
        }
        .navbar .dropdown {
            display: block;
            visibility: visible;
            transition: all 0.2s ease-in-out;
        } .dropdown .nav {
            font-family: subtext;
            width: 100%;
            height: 50px;
            border-left: 1px solid white;
            border-right: 1px solid white;
            justify-content: center;
            font-size: 1.5em;
            display: flex;
            align-items: center;
            text-decoration: none;
            color: black;
            font-weight: 850;
            transition: all 0.2s ease-in-out;
            background-color: white;
        } .dropdown .nav:active {
            color: white;
            cursor: pointer;
        } .dropdown .navdrop {
            background-color: white;
            width: 100px;
            height: 50px;
            color: black;
            font-family: primary;
            font-size: 1.5rem;
            border-left: 2px solid white;
            border-right: 2px solid white;
            display: flex;
            justify-content: center;
        } .dropdown .navdrop span {
            width: 5em;
            height: 2.5em;
        }
    }
</style>