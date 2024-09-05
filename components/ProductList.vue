<template>
    <div class="bg-white">
        <div class="mx-auto px-1 py-2 sm:px-2 sm:py-4 lg:max-w-1xl lg:px-8">
            <div class="mt-3 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-2 xl:gap-x-8">
                <div v-for="product in productList" :key="product.id" class="group relative cursor-pointer">
                    <div
                        class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-50">
                        <img :src="product.img" :alt="product.imageAlt"
                            class="h-full w-full object-cover object-center lg:h-full lg:w-full" />
                    </div>
                    <div class="flex mt-2">
                        <span v-for="star in product.rating" class="mt-1">
                            <svg class="w-4 h-4 text-yellow-300 me-1" aria-hidden="true"
                                xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
                                <path
                                    d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z" />
                            </svg>
                        </span>
                        ({{ product.reviewCount }})
                    </div>
                    <div class="flex justify-between">
                        <div>
                            <h3 class="text-base font-medium text-gray-700">
                                <a :href="product.href">
                                    {{ product.name }}
                                </a>
                            </h3>
                            <p class="mt-1 text-sm text-gray-500">{{ product.color }}</p>
                        </div>
                    </div>
                    <div class="text-lg font-medium text-gray-900">
                        <span class="line-through">${{ product.discountPrice }}</span>
                        <span class="ml-1">${{ product.actualPrice }}</span>
                    </div>
                </div>
            </div>
            <div class="flex justify-center w-full mt-10">
                <button type="button"
                    class="flex text-black hover:text-white border border-gray-800 hover:bg-gray-200 focus:ring-4 focus:outline-none focus:ring-gray-300 font-medium rounded-xl text-sm px-5 py-2.5 text-center me-2 mb-2 dark:border-gray-600 dark:text-black dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-gray-800">
                    <span class="mr-2">View more</span>
                    <svg fill="#000000" height="15px" width="15px" version="1.1" id="Layer_1"
                        xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                        viewBox="0 0 330 210" xml:space="preserve">
                        <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                        <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                        <g id="SVGRepo_iconCarrier">
                            <path id="XMLID_225_"
                                d="M325.607,79.393c-5.857-5.857-15.355-5.858-21.213,0.001l-139.39,139.393L25.607,79.393 c-5.857-5.857-15.355-5.858-21.213,0.001c-5.858,5.858-5.858,15.355,0,21.213l150.004,150c2.813,2.813,6.628,4.393,10.606,4.393 s7.794-1.581,10.606-4.394l149.996-150C331.465,94.749,331.465,85.251,325.607,79.393z">
                            </path>
                        </g>
                    </svg>
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
const productList = [
    {
        id: 1,
        name: "Tien Full Shirt",
        rating: 4,
        reviewCount: 24,
        actualPrice: 15,
        discountPrice: 30,
        img: "https://ih1.redbubble.net/image.5099453350.8283/ssrco,slim_fit_t_shirt,womens,fafafa:ca443f4786,front,square_product,600x600.jpg",
    },
    {
        id: 2,
        name: "Gohan Half Shirt",
        rating: 5,
        reviewCount: 78,
        actualPrice: 17,
        discountPrice: 25,
        img: "https://ih1.redbubble.net/image.4561075948.3630/ssrco,classic_tee,womens,fafafa:ca443f4786,front_alt,square_product,600x600.u2.jpg",
    },
    {
        id: 3,
        name: "Goku Keychain",
        rating: 4,
        reviewCount: 45,
        actualPrice: 90,
        discountPrice: 120,
        img: "https://ih1.redbubble.net/image.5577171159.1568/st,small,507x507-pad,600x600,f8f8f8.jpg",
    },
    {
        id: 4,
        name: "Shien Vest Plates",
        rating: 3,
        reviewCount: 23,
        actualPrice: 30,
        discountPrice: 37,
        img: "https://ih1.redbubble.net/image.746781885.8307/st,small,507x507-pad,600x600,f8f8f8.u4.jpg",
    },
];
</script>
