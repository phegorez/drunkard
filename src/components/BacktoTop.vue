<template>
    <div class="absolute bg-[#202235] right-12 lg:bottom-[-182.75rem] xl:bottom-[-175.75rem] sm:hidden lg:block p-4 rounded-[50%] cursor-pointer" v-if="showButton" @click="scrollToTop">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 8L1.41 9.41L7 3.83L7 16H9V3.83L14.59 9.41L16 8L8 0L0 8Z" fill="#3DDEED"/>
        </svg>
    </div>
</template>
<script setup>
import {ref, onMounted, onBeforeMount} from 'vue'
const showButton = ref(false)

const handleScroll = () => {
    showButton.value = window.scrollY > 100
}

const scrollToTop = () => {
    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    })
}
onMounted(() => {
    window.addEventListener('scroll', handleScroll)
}),

onBeforeMount(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>
