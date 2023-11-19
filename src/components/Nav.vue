<template>
    <nav class="nav">

        <div class="hamburger-menu">
            <svg width="19" height="12" viewBox="0 0 19 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M0.5 12H18.5V10H0.5V12ZM0.5 7H18.5V5H0.5V7ZM0.5 0V2H18.5V0H0.5Z" fill="white" />
            </svg>
        </div>
        <Menu class="sm:hidden lg:block"/>

        <div class="font-bold text-[20px] relative lg:right-14">
            <span class="text-[#8EFFC9]">Drunkard</span> <span>Remiex</span>
        </div>

        <SearchBar />
    </nav>
</template>
<script setup>
import SearchBar from './SearchBar.vue';
import Menu from './Menu.vue'
</script>
