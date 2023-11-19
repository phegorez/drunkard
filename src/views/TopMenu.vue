<template>
    <section class="topMenu-section">
        <TopMenuHeader />
        <div class="flex flex-col gap-8 justify-center items-center lg:mt-32 sm:mt-16 lg:px-0">
            <TopMenuCard />
            <Pagination />
        </div>
    </section>
</template>
<script setup>
import Pagination from '../components/Pagination.vue';
import TopMenuCard from '../components/TopMenuCard.vue';
import TopMenuHeader from '../components/TopMenuHeader.vue'
</script>
