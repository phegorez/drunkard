<template>
    <div class="pagination">
        <ul class="flex">
            <li class="btn prev flex flex-col justify-center" @click="decrementDouble" v-if="page > 1">
                <span><svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M12.6233 3.43222C12.7607 3.4293 12.8955 3.4754 13.009 3.56416C13.1226 3.65291 13.2093 3.77992 13.2571 3.92761C13.3049 4.07531 13.3114 4.23638 13.2759 4.38855C13.2403 4.54071 13.1644 4.67644 13.0585 4.77695L9.00898 8.75095L13.061 12.7249C13.1351 12.7868 13.1971 12.8656 13.2432 12.9563C13.2894 13.047 13.3186 13.1477 13.3291 13.2521C13.3395 13.3564 13.331 13.4621 13.3041 13.5624C13.2771 13.6628 13.2323 13.7557 13.1725 13.8352C13.1127 13.9147 13.0391 13.9792 12.9565 14.0244C12.8738 14.0697 12.7839 14.0949 12.6923 14.0983C12.6008 14.1018 12.5096 14.0834 12.4245 14.0445C12.3394 14.0055 12.2624 13.9467 12.1981 13.8718L7.56575 9.333C7.4929 9.26167 7.4344 9.17308 7.39429 9.07334C7.35419 8.9736 7.33341 8.86508 7.33341 8.75525C7.33342 8.64542 7.35419 8.5369 7.39429 8.43716C7.4344 8.33742 7.4929 8.24883 7.56575 8.1775L12.1981 3.62432C12.3155 3.50453 12.4662 3.43644 12.6233 3.43222Z"
                            fill="#AFB9C3" />
                        <path
                            d="M7.95665 3.43222C8.09405 3.4293 8.22885 3.4754 8.34238 3.56416C8.45592 3.65291 8.54258 3.77992 8.59038 3.92761C8.63819 4.07531 8.64476 4.23638 8.60919 4.38855C8.57363 4.54071 8.49768 4.67644 8.39187 4.77695L4.34232 8.75095L8.39437 12.7249C8.4684 12.7868 8.53044 12.8656 8.57657 12.9563C8.6227 13.047 8.65193 13.1477 8.6624 13.2521C8.67288 13.3564 8.66437 13.4621 8.63742 13.5624C8.61048 13.6628 8.56568 13.7557 8.50584 13.8352C8.44601 13.9147 8.37245 13.9792 8.2898 14.0244C8.20715 14.0697 8.11721 14.0949 8.02565 14.0983C7.93409 14.1018 7.8429 14.0834 7.75784 14.0445C7.67277 14.0055 7.59569 13.9467 7.53144 13.8718L2.89908 9.333C2.82623 9.26167 2.76774 9.17308 2.72763 9.07334C2.68752 8.9736 2.66675 8.86508 2.66675 8.75525C2.66675 8.64542 2.68752 8.5369 2.72763 8.43716C2.76774 8.33742 2.82623 8.24883 2.89908 8.1775L7.53143 3.62432C7.64882 3.50453 7.79953 3.43644 7.95665 3.43222Z"
                            fill="#AFB9C3" />
                    </svg>
                </span>
            </li>

            <li class="btn prev flex flex-col justify-center" @click="decrementPage" v-if="page > 1">
                <span><svg width="8" height="13" viewBox="0 0 8 13" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M7.5 11.228L3.17341 6.76546L7.5 2.30296L6.16802 0.932129L0.5 6.76546L6.16802 12.5988L7.5 11.228Z"
                            fill="#AFB9C3" />
                    </svg>
                </span>
            </li>

            <li class="numb" @click="changePage(1)" v-if="page > 2">
                <span>1</span>
            </li>

            <li class="dots" v-if="page > 3">
                <span>...</span>
            </li>

            <li class="numb" v-for="pageNumber in pagesToShow" :key="pageNumber" @click="changePage(pageNumber)"
                :class="{ active: page === pageNumber, numb: true }">
                <span>{{ pageNumber }}</span>
            </li>

            <li class="dots" v-if="page < totalPages - 2">
                <span>...</span>
            </li>

            <li class="numb" @click="changePage(totalPages)" v-if="page < totalPages - 1">
                <span>{{ totalPages }}</span>
            </li>

            <li class="btn next flex flex-col justify-center" @click="incrementPage" v-if="page < totalPages">
                <span><svg width="14" height="15" viewBox="0 0 14 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M3.5 12.228L7.82659 7.76546L3.5 3.30296L4.83198 1.93213L10.5 7.76546L4.83198 13.5988L3.5 12.228Z"
                            fill="#AFB9C3" />
                    </svg>
                </span>
            </li>

            <li class="btn next flex flex-col justify-center" @click="incrementDouble" v-if="page < totalPages">
                <span><svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M1.37668 0.432219C1.23928 0.429298 1.10449 0.475404 0.990952 0.564157C0.877416 0.652909 0.79075 0.779921 0.74295 0.927614C0.695149 1.07531 0.688577 1.23638 0.724141 1.38855C0.759705 1.54071 0.83565 1.67644 0.941463 1.77695L4.99102 5.75095L0.938962 9.72494C0.864935 9.7868 0.802897 9.86558 0.756765 9.95631C0.710632 10.047 0.681407 10.1477 0.670933 10.2521C0.660459 10.3564 0.668963 10.4621 0.69591 10.5624C0.722856 10.6628 0.767658 10.7557 0.827491 10.8352C0.887322 10.9147 0.960885 10.9792 1.04354 11.0244C1.12619 11.0697 1.21613 11.0949 1.30769 11.0983C1.39925 11.1018 1.49044 11.0834 1.5755 11.0445C1.66056 11.0055 1.73765 10.9467 1.8019 10.8718L6.43425 6.333C6.5071 6.26167 6.5656 6.17308 6.60571 6.07334C6.64582 5.9736 6.66659 5.86508 6.66659 5.75525C6.66659 5.64542 6.64582 5.5369 6.60571 5.43716C6.5656 5.33742 6.5071 5.24883 6.43425 5.1775L1.8019 0.624323C1.68451 0.504525 1.53381 0.43644 1.37668 0.432219Z"
                            fill="#AFB9C3" />
                        <path
                            d="M6.04335 0.432219C5.90595 0.429298 5.77116 0.475404 5.65762 0.564157C5.54408 0.65291 5.45742 0.779921 5.40962 0.927615C5.36182 1.07531 5.35524 1.23638 5.39081 1.38855C5.42637 1.54071 5.50232 1.67644 5.60813 1.77695L9.65768 5.75095L5.60563 9.72494C5.5316 9.7868 5.46956 9.86558 5.42343 9.95631C5.3773 10.047 5.34807 10.1477 5.3376 10.2521C5.32713 10.3564 5.33563 10.4621 5.36258 10.5624C5.38952 10.6628 5.43432 10.7557 5.49416 10.8352C5.55399 10.9147 5.62755 10.9792 5.7102 11.0244C5.79285 11.0697 5.88279 11.0949 5.97435 11.0983C6.06591 11.1018 6.1571 11.0834 6.24216 11.0445C6.32723 11.0055 6.40432 10.9467 6.46857 10.8718L11.1009 6.333C11.1738 6.26167 11.2323 6.17308 11.2724 6.07334C11.3125 5.9736 11.3333 5.86508 11.3333 5.75525C11.3333 5.64542 11.3125 5.5369 11.2724 5.43716C11.2323 5.33742 11.1738 5.24883 11.1009 5.1775L6.46857 0.624323C6.35118 0.504526 6.20047 0.43644 6.04335 0.432219Z"
                            fill="#AFB9C3" />
                    </svg>

                </span>
            </li>
        </ul>
    </div>
</template>

<script setup>
import { ref, computed } from 'vue'

// Reactive variables
const totalPages = ref(10) // Number of total pages
const page = ref(1) // Currently selected page

// Methods to change the page
const incrementPage = () => {
    // Increase the page number if not already at the last page
    if (page.value < totalPages.value) {
        page.value++
    }
}

const incrementDouble = () => {
    // Increase 2 page number if page less than 9 
    if (page.value < 9) {
        page.value += 2
    } else if(page.value < totalPages.value) {
        page.value++
    }
}

const decrementPage = () => {
    // Decrease the page number if not already at the first page
    if (page.value > 1) {
        page.value--
    }
}

const decrementDouble = () => {
    if (page.value > 2 ) {
        page.value -= 2
    } else if (page.value > 1) {
        page.value --
    }
}


const changePage = (newPage) => {
    // Change the page to the specified value within the valid range
    if (newPage >= 1 && newPage <= totalPages.value) {
        page.value = newPage
    }
    console.log(`Current Page: ${page.value}`);
}

// Computed property to calculate which pages to show
const pagesToShow = computed(() => {
    let beforePages = page.value - 1
    let afterPages = page.value + 1

    // Adjust beforePages and afterPages based on the current page position
    if (page.value === totalPages.value) {
        beforePages = beforePages - 2
    } else if (page.value === totalPages.value - 1) {
        beforePages = beforePages - 1
    }

    if (page.value === 1) {
        afterPages = afterPages + 2
    } else if (page.value === 2) {
        afterPages = afterPages + 1
    }

    const pages = []
    for (let pageNumber = beforePages; pageNumber <= afterPages; pageNumber++) {
        if (pageNumber > 0 && pageNumber <= totalPages.value) {
            pages.push(pageNumber)
        }
    }

    return pages
})
</script>

<style></style>
