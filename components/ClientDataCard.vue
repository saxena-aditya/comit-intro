<script setup>
const { imgWidth, imgHeight, item } = defineProps([
    "imgWidth",
    "imgHeight",
    "item",
]);
</script>
<template>
    <div class="shadow dark:bg-gray-100">
        <a href="#">
            <img :src="`https://picsum.photos/${imgWidth}/${imgHeight}`" alt="" class="w-full" />
        </a>

        <div class="p-3" v-if="!item.fullImage">
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-800">
                Here are the biggest enterprise technology acquisitions of 2021 so far,
                in reverse chronological order.
            </p>
        </div>
    </div>
</template>
