<template>
    <footer class="bg-[#202235] p-20">
        <div class="flex justify-center gap-64">
            <div class="flex flex-row gap-20">
                <div class="flex flex-col gap-6">
                    <div class="font-bold text-[20px]">
                        <span class="text-[#8EFFC9]">Drunkard</span> <span class="text-white">Remiex</span>
                    </div>
                    <div class="flex justify-between">
                        <svg width="18" height="16" viewBox="0 0 18 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M12.2861 0C10.1822 0 8.47671 1.79086 8.47671 4C8.47671 4.33382 8.51565 4.65809 8.58903 4.96808C6.56611 4.96808 3.51914 4.55908 0.974438 2.00961C0.636055 1.67059 0.0120846 1.89726 0.035556 2.37567C0.412681 10.0627 3.70477 12.3049 5.4001 12.4444C4.30535 13.5257 2.7151 14.3791 1.11489 14.7622C0.692564 14.8633 0.588236 15.3256 1.0012 15.4599C2.14623 15.8323 3.78516 15.9758 4.66735 16C10.9082 16 15.9806 10.7471 16.0935 4.22229C16.9129 3.68945 17.4377 2.5325 17.7326 1.71291C17.8044 1.5133 17.4773 1.28073 17.2815 1.36226C16.6694 1.61708 15.8923 1.67749 15.2304 1.46181C14.5318 0.569266 13.4722 0 12.2861 0Z"
                                fill="white" />
                        </svg>

                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd"
                                d="M5 0C2.23858 0 0 2.23858 0 5V15C0 17.7614 2.23858 20 5 20H15C17.7614 20 20 17.7614 20 15V5C20 2.23858 17.7614 0 15 0H5ZM16 5C16.5523 5 17 4.55228 17 4C17 3.44772 16.5523 3 16 3C15.4477 3 15 3.44772 15 4C15 4.55228 15.4477 5 16 5ZM15 10C15 12.7614 12.7614 15 10 15C7.23858 15 5 12.7614 5 10C5 7.23858 7.23858 5 10 5C12.7614 5 15 7.23858 15 10ZM10 13C11.6569 13 13 11.6569 13 10C13 8.34315 11.6569 7 10 7C8.34315 7 7 8.34315 7 10C7 11.6569 8.34315 13 10 13Z"
                                fill="white" />
                        </svg>

                        <svg width="22" height="16" viewBox="0 0 22 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M18.2701 1.33005C16.9401 0.710046 15.5001 0.260046 14.0001 4.59982e-05C13.987 -0.000374605 13.9739 0.00209348 13.9618 0.00727676C13.9497 0.01246 13.9389 0.0202326 13.9301 0.0300462C13.7501 0.360046 13.5401 0.790046 13.4001 1.12005C11.8091 0.880046 10.1911 0.880046 8.60012 1.12005C8.46012 0.780046 8.25012 0.360046 8.06012 0.0300462C8.05012 0.0100462 8.02012 4.59982e-05 7.99012 4.59982e-05C6.49012 0.260046 5.06012 0.710046 3.72012 1.33005C3.71012 1.33005 3.70012 1.34005 3.69012 1.35005C0.970117 5.42005 0.220117 9.38004 0.590117 13.3C0.590117 13.32 0.600117 13.34 0.620117 13.35C2.42012 14.67 4.15012 15.47 5.86012 16C5.89012 16.01 5.92012 16 5.93012 15.98C6.33012 15.43 6.69012 14.85 7.00012 14.24C7.02012 14.2 7.00012 14.16 6.96012 14.15C6.39012 13.93 5.85012 13.67 5.32012 13.37C5.28012 13.35 5.28012 13.29 5.31012 13.26C5.42012 13.18 5.53012 13.09 5.64012 13.01C5.66012 12.99 5.69012 12.99 5.71012 13C9.15012 14.57 12.8601 14.57 16.2601 13C16.2801 12.99 16.3101 12.99 16.3301 13.01C16.4401 13.1 16.5501 13.18 16.6601 13.27C16.7001 13.3 16.7001 13.36 16.6501 13.38C16.1301 13.69 15.5801 13.94 15.0101 14.16C14.9701 14.17 14.9601 14.22 14.9701 14.25C15.2901 14.86 15.6501 15.44 16.0401 15.99C16.0701 16 16.1001 16.01 16.1301 16C17.8501 15.47 19.5801 14.67 21.3801 13.35C21.4001 13.34 21.4101 13.32 21.4101 13.3C21.8501 8.77004 20.6801 4.84005 18.3101 1.35005C18.3001 1.34005 18.2901 1.33005 18.2701 1.33005ZM7.52012 10.91C6.49012 10.91 5.63012 9.96005 5.63012 8.79005C5.63012 7.62005 6.47012 6.67005 7.52012 6.67005C8.58012 6.67005 9.42012 7.63005 9.41012 8.79005C9.41012 9.96005 8.57012 10.91 7.52012 10.91ZM14.4901 10.91C13.4601 10.91 12.6001 9.96005 12.6001 8.79005C12.6001 7.62005 13.4401 6.67005 14.4901 6.67005C15.5501 6.67005 16.3901 7.63005 16.3801 8.79005C16.3801 9.96005 15.5501 10.91 14.4901 10.91Z"
                                fill="white" />
                        </svg>

                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M20 10C20 4.48 15.52 0 10 0C4.48 0 0 4.48 0 10C0 14.84 3.44 18.87 8 19.8V13H6V10H8V7.5C8 5.57 9.57 4 11.5 4H14V7H12C11.45 7 11 7.45 11 8V10H14V13H11V19.95C16.05 19.45 20 15.19 20 10Z"
                                fill="white" />
                        </svg>
                    </div>
                    <h4 class="text-white">(+994) 199-28-786</h4>
                </div>

                <div class="flex gap-20">
                    <div class="flex flex-col gap-4">
                        <h2 class="font-bold text-white text-lg">Drunkard Navigation</h2>
                        <ul class="flex flex-col gap-4">
                            <li class="text-white">Home</li>
                            <li class="text-white">Recipes</li>
                            <li class="text-white">Cocktail Language</li>
                            <li class="text-white">Recommend</li>
                        </ul>
                    </div>
                    <div class="flex flex-col gap-4">
                        <h2 class="font-bold text-white text-lg">About us</h2>
                        <ul class="flex flex-col gap-4">
                            <li class="text-white">Login</li>
                            <li class="text-white">Sign Up</li>
                            <li class="text-white">Privacy</li>
                            <li class="text-white">Contact</li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="flex flex-col gap-5">
                <h2 class="font-bold text-white text-lg">Subscribe Our News Letter</h2>
                <p class="w-96 text-white">Sure, please provide your email address to subscribe to newsletter</p>
                <div class="border rounded-md">
                    <input type="text" placeholder="Enter your mail..." class="input">
                    <button class="bg-[#3DDEED] p-4 border-none ml-2 rounded-r-md font-bold">Subscribe</button>
                </div>
            </div>
        </div>
        <p class="text-center mt-16 text-white">© 2023 Your Company Name. All rights reserved.</p>
    </footer>
</template>
<script setup>

</script>