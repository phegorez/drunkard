<template>
    <div class="search-bar">
            <input type="text" class="input" placeholder="Search recipes or cocktail.." :class="isSearchToggle ? 'sm:absolute sm:top-3 sm:right-[5.2rem] md:w-4/5 sm:transition-all' : 'sm:hidden lg:block'">
            <svg class="w-6 h-6 text-[#AFB9C3] dark:text-white lg:mr-4 sm:cursor-pointer" @click="toggleSearch" width="23" height="22"
                viewBox="0 0 23 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="11.2861" cy="10.786" r="8.23951" stroke="#BEAFC3" stroke-width="1.5" stroke-linecap="round"
                    stroke-linejoin="round" />
                <path d="M17.0168 16.9447L20.2472 20.1667" stroke="#BEAFC3" stroke-width="1.5" stroke-linecap="square"
                    stroke-linejoin="round" />
            </svg>
        </div>
</template>
<script setup>
import { ref } from 'vue';
const isSearchToggle = ref(false)
const windowSize = ref(window.innerWidth)
const toggleSearch = () => {
    if(windowSize.value <= 768) {
        isSearchToggle.value = !isSearchToggle.value
    }
}

console.log(windowSize.value)

</script>
