<script setup>
import { ref } from "vue";

var isLoading = ref(false);
const update = () => {
    console.log("update called");
    isLoading.value = !isLoading.value;
    const router = useRouter();
    setTimeout(() => {
        router.push({ path: "/home" });
    }, 3000);
};
</script>
<template>
    <div>
        <div class="flex flex-col p-2 py-6 m-h-screen h-screen bg-black justify-center items-center">
            <div class="text-center text-white">
                <div class="image">
                    <img class="w-96 pb-4"
                        src="https://cdn.prod.website-files.com/646e1a4461befb4982487d18/64ba4f3bd6fe425eb91aba41_Logo.svg" />
                </div>
            </div>
            <div class="text-4xl text-white pb-8">
                turning <span class="full-grad">point of inspiration</span> into
                <span class="full-grad">point of sale</span>
            </div>
            <div class="bg-white items-center justify-between w-full flex rounded-full shadow-lg p-2 mb-5 sticky sm:w-3/5"
                style="top: 5px">
                <div>
                    <div class="p-2 mr-1 ml-1 rounded-full hover:bg-gray-100 cursor-pointer">
                        <svg class="w-8 h-8 text-black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"
                            fill="currentColor">
                            <path fill-rule="evenodd"
                                d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                                clip-rule="evenodd" />
                        </svg>
                    </div>
                </div>

                <input
                    class="font-medium rounded-full w-full py-4 pl-4 text-black leading-tight focus:outline-none focus:shadow-outline lg:text-2xl sm:w-full"
                    type="text" placeholder="Start by typing your brand name" />

                <div class="bg-gray-600 p-2 hover:bg-[#f05596] cursor-pointer mx-2 rounded-full">
                    <svg class="w-12 h-8 text-white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 17"
                        fill="currentColor">
                        <path d="M5 3a3 3 0 0 1 6 0v5a3 3 0 0 1-6 0z" />
                        <path
                            d="M3.5 6.5A.5.5 0 0 1 4 7v1a4 4 0 0 0 8 0V7a.5.5 0 0 1 1 0v1a5 5 0 0 1-4.5 4.975V15h3a.5.5 0 0 1 0 1h-7a.5.5 0 0 1 0-1h3v-2.025A5 5 0 0 1 3 8V7a.5.5 0 0 1 .5-.5" />
                    </svg>
                </div>
            </div>
            <button
                class="relative mt-5 text-white bg-gradient-to-r from-purple-500 to-pink-500 hover:bg-gradient-to-l focus:ring-4 focus:outline-none focus:ring-purple-200 dark:focus:ring-purple-800 font-medium rounded-full text-xl px-20 py-3 text-center inline-flex items-center me-2 mb-2"
                v-on:click.prevent="update">
                <svg v-if="isLoading" aria-hidden="true" role="status"
                    class="inline w-6 h-6 me-2 text-white animate-spin" viewBox="0 0 100 101" fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z"
                        fill="#E5E7EB" />
                    <path
                        d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z"
                        fill="currentColor" />
                </svg>
                <span v-if="!isLoading" class="w-full flex items-center">Create my Store
                    <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                        fill="none" viewBox="0 0 14 10">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M1 5h12m0 0L9 1m4 4L9 9" />
                    </svg></span>
                <span v-else class="w-full flex items-center">
                    Gathering your brand info...
                </span>
            </button>
        </div>
    </div>
</template>
