<template>
    <section class="px-64 py-28 bg-black">
        <TopMenuHeader />
        <div class="flex flex-col gap-8 justify-center items-center mt-32 px-72">
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
