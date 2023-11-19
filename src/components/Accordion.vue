<template>
    <div class="w-full bg-[#202235] rounded-xl mb-6" v-for="(item, index) in AccordionInfor" :key="item.id">
        <div class="flex items-center xl:text-[1.5rem] sm:text-[1rem] justify-between w-full lg:font-bold text-white lg:p-8 sm:px-6 md:px-2 sm:py-3 cursor-pointer"
            @click="accordionOpen(item.id)">
            <h2>{{ item.inforTitle }}</h2>
            <svg class="w-6 h-2 text-white" v-if="!item.isOpen" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
                viewBox="0 0 10 6">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="m1 1 4 4 4-4" />
            </svg>
            <svg class="w-6 h-2 text-[#3DDEED]" v-else aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                fill="none" viewBox="0 0 10 6">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M9 5 5 1 1 5" />
            </svg>
        </div>
        <div :class="item.isOpen ? 'block' : 'hidden'" class="p-8 text-white text-[1.125rem]">
            <p>
                {{ item.inforDetail }}
            </p>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const AccordionInfor = ref([
    {
        id: 1,
        inforTitle: 'Find cocktails near me',
        inforDetail: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        isOpen: false
    },
    {
        id: 2,
        inforTitle: 'Do I need drinking more or for longer than intended?',
        inforDetail: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        isOpen: false
    },
    {
        id: 3,
        inforTitle: 'What’s the Difference Between a Mixologist and a Bartender?',
        inforDetail: '“Mixology” is that the word is often used interchangeably with “Bartending.” There is a large overlap in the skill set required for a great bartender and a master Mixologist, but they are distinct roles. A bartender generally works at a cocktail bar making classic cocktails and house specialties, while also interacting directly with customers in ways similar to a restaurant server. Mixologists may work occasionally in a bartending capacity, but their job title implies that they do a significant portion of their job behind the scenes, creating new craft cocktails and putting their signature twist on existing favorites..',
        isOpen: false
    },
    {
        id: 4,
        inforTitle: 'What are the main ingredients of cocktail?',
        inforDetail: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        isOpen: false
    },
])

const accordionOpen = (id) => {
    let accordioninfo = AccordionInfor.value

    //Find the item with the given id
    const item = accordioninfo.find((item) => item.id === id)

    // Toggle the isOpen property
    if (item) {
        item.isOpen = !item.isOpen;
    }
}

</script>
