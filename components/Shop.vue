<template>
    <section class="flex sm:py-10 border w-fit sm:py-10 sm:px-10 relative">
        <div class="absolute text-white bg-black border-text text-xl flex invisible sm:visible">
            <span class="py-1 mr-2">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                    class="bi bi-graph-up" viewBox="0 0 16 16">
                    <path fill-rule="evenodd"
                        d="M0 0h1v15h15v1H0zm14.817 3.113a.5.5 0 0 1 .07.704l-4.5 5.5a.5.5 0 0 1-.74.037L7.06 6.767l-3.656 5.027a.5.5 0 0 1-.808-.588l4-5.5a.5.5 0 0 1 .758-.06l2.609 2.61 4.15-5.073a.5.5 0 0 1 .704-.07" />
                </svg>
            </span>
            <span class="full-grad "> Satellite stores excelerate conversions</span>
        </div>
        <div class="sm:w-96 shop-h overflow-auto scrollbar-hide rounded-lg">
            <HeroVideo />
            <ProductList />
            <ShopFooter />
        </div>
    </section>
</template>

<style scoped>
.shop-h {
    height: 682px;
}

.scrollbar-hide::-webkit-scrollbar {
    display: none;
}

.scrollbar-hide {
    -ms-overflow-style: none;
    /* IE and Edge */
    scrollbar-width: none;
    /* Firefox */
}

.product-container {
    position: absolute;
    width: 100%;
    bottom: 0;
    padding: 0px 12px;
}

.border-text {
    top: -35px;
    background-color: black;
    padding: 20px 15px;
}
</style>
