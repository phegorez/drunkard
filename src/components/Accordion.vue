<template>
    <div class="w-2/4 bg-[#202235] rounded-xl mb-6" v-for="(item, index) in AccordionInfor" :key="item.id">
        <button class="flex items-center text-[24px] justify-between w-full font-bold text-white p-8"
            @click="accordionOpen(item.id)">{{ item.inforTitle }}<svg width="31" height="31" viewBox="0 0 31 31" fill="none"
                xmlns="http://www.w3.org/2000/svg">
                <path
                    :d="item.isOpen ? 'M5.16667 15.5L6.98792 17.3212L14.2083 10.1137L14.2083 25.8333H16.7917V10.1137L24.0121 17.3212L25.8333 15.5L15.5 5.16667L5.16667 15.5' : 'M25.8333 15.5L24.012 13.6787L16.7916 20.8862V5.16663H14.2083L14.2083 20.8862L6.98783 13.6787L5.16658 15.5L15.4999 25.8333L25.8333 15.5Z'"
                    :fill="item.isOpen ? '#3DDEED' : 'white'" />
            </svg>
        </button>
        <div :class="item.isOpen ? 'block' : 'hidden'" class="p-8 text-white text-[18px]">
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
        id : 1,
        inforTitle : 'Find cocktails near me',
        inforDetail : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        isOpen : false
    },
    {
        id : 2,
        inforTitle : 'Do I need drinking more or for longer than intended?',
        inforDetail : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        isOpen : false
    },
    {
        id : 3,
        inforTitle : 'What’s the Difference Between a Mixologist and a Bartender?',
        inforDetail : '“Mixology” is that the word is often used interchangeably with “Bartending.” There is a large overlap in the skill set required for a great bartender and a master Mixologist, but they are distinct roles. A bartender generally works at a cocktail bar making classic cocktails and house specialties, while also interacting directly with customers in ways similar to a restaurant server. Mixologists may work occasionally in a bartending capacity, but their job title implies that they do a significant portion of their job behind the scenes, creating new craft cocktails and putting their signature twist on existing favorites..',
        isOpen : false
    },
    {
        id : 4,
        inforTitle : 'What are the main ingredients of cocktail?',
        inforDetail : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        isOpen : false
    },
])

const accordionOpen = (id) => {
    let accordioninfo = AccordionInfor.value

    //Find the item with the given id
    const item = accordioninfo.find((item) => item.id === id)

    // Toggle the isOpen property
    if(item) {
        item.isOpen = !item.isOpen;
    }
}

</script>
