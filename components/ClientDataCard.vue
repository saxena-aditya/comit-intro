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
            <img :src="item.img" alt="" class="w-full" />
        </a>
        <div class="font-bold text-sm text-black pl-2 pt-2" v-if="!item.fullImage">Dragon Ball Z</div>
        <div class="font-medium text-sm text-gray-500 pl-2" v-if="!item.fullImage">@dbz.tshirts</div>
        <div class="p-2" v-if="!item.fullImage">
            <p class="mb-3 font-normal text-gray-900 dark:text-gray-900">
                {{ item.desc }}
            </p>
        </div>
    </div>
</template>
