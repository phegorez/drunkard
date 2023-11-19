<template>
    <nav class="nav">

        <div class="hamburger-menu" @click="toggleMenu">
            <svg width="19" height="12" viewBox="0 0 19 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M0.5 12H18.5V10H0.5V12ZM0.5 7H18.5V5H0.5V7ZM0.5 0V2H18.5V0H0.5Z" fill="white" />
            </svg>
        </div>

        <ul
            :class="isToggle ? 'sm:flex sm:flex-col sm:absolute sm:top-16 sm:left-0 sm:bg-[#13152A] sm:w-full sm:gap-4 sm:p-8 sm:transition-all sm:z-50' : 'lg:flex sm:hidden'">
            <li class="mr-6"><a href="#" class="hover:text-gray-300 on-click">Home</a></li>
            <li class="mr-6"><a href="#" class="hover:text-gray-300 on-click">Recipes</a></li>
            <li class="mr-6"><a href="#" class="hover:text-gray-300 on-click">Cocktail Language</a></li>
            <li><a href="#" class="hover:text-gray-300 on-click">Contact</a></li>
        </ul>

        <div class="font-bold text-[20px] relative lg:right-14 sm:right-13">
            <span class="text-[#8EFFC9]">Drunkard</span> <span>Remiex</span>
        </div>

        <SearchBar />
    </nav>
</template>
<script setup>
import { ref } from 'vue';
import SearchBar from './SearchBar.vue'

const isToggle = ref(false)

const toggleMenu = () => {
    isToggle.value = !isToggle.value
}

</script>
