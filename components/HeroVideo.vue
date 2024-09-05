<template>
  <div class="video-container relative shadow-ld shadow-white">
    <div class="w-full bg-gray-400 rounded-full h-1 dark:bg-gray-400 absolute top-0 ani">
      <div class="bg-white h-1 rounded-full ani" :style="{ width: videoProgress + '%' }"></div>
    </div>
    <video ref="video" autoplay paused @click="toggel" @timeupdate="updateVideoProgress" class="cursor-pointer"
      src="https://res.cloudinary.com/di5mptsqz/video/upload/q_auto/f_webm/v1700822389/production/brand_ZTkeeR9tRpRdBKj7/jrpr98ljs5g74rzk3pzx"></video>
    <div>
      <div class="flex flex-col product-container">
        <div class="flex flex-row items-center bg-black opacity-70 shadow md:flex-row md:max-w-xl rounded-lg">
          <img
            class="object-cover w-24 sm:w-full rounded-t-lg sm:h-96 md:h-auto md:w-28 md:rounded-none md:rounded-s-lg"
            src="https://i.pinimg.com/736x/fc/49/aa/fc49aab2ebcb5e9e658d673bdda8392c.jpg" alt="" />
          <div class="flex flex-col p-2 leading-normal ">
            <h5 class="mb-1 text-base font-medium text-white sm:text-xl">
              Dragon Ball Z T-shirt
            </h5>

            <div class="flex items-center">
              <svg class="w-4 h-4 text-yellow-300 me-1" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                fill="currentColor" viewBox="0 0 22 20">
                <path
                  d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z" />
              </svg>
              <svg class="w-4 h-4 text-yellow-300 me-1" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                fill="currentColor" viewBox="0 0 22 20">
                <path
                  d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z" />
              </svg>
              <svg class="w-4 h-4 text-yellow-300 me-1" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                fill="currentColor" viewBox="0 0 22 20">
                <path
                  d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z" />
              </svg>
              <svg class="w-4 h-4 text-yellow-300 me-1" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                fill="currentColor" viewBox="0 0 22 20">
                <path
                  d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z" />
              </svg>
              <svg class="w-4 h-4 text-yellow-300 me-1" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                fill="currentColor" viewBox="0 0 22 20">
                <path
                  d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 9.2a1.523 1.523 0 0 0 .387-1.575Z" />
              </svg>
              <p class="ms-2 text-sm font-bold text-gray-900 dark:text-white">
                4.95
              </p>
              <span class="w-1 h-1 mx-1.5 bg-gray-500 rounded-full dark:bg-gray-400"></span>
              <a href="#" class="text-sm font-medium text-gray-900 hover:no-underline dark:text-white">(73)</a>
            </div>
            <div>
              <span class="text-sm sm:text-lg font-medium text-gray-900 line-through dark:text-white">$109</span><span
                class="ms-1 sm:text-lg text-sm font-medium text-gray-900 dark:text-white">$79</span>
            </div>
            <a href="#"
              class="text-black flex justify-center border sm:m-4 p-2 bg-white opacity-100 font-bold rounded-md w-full hover:bg-gray-200">View
              Product</a>
          </div>
        </div>
        <div class="flex justify-center text-white font-bold text-lg py-3">Swipe up to store <span class="p-2">
            <svg viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg" class="rotate-180 w-4 h-4"
              filled="">
              <path d="M14 4 8.5 8.667 3 4m11 4.333L8.5 13 3 8.333" stroke="#fff" stroke-linecap="round"
                stroke-linejoin="round"></path>
            </svg>
          </span></div>
      </div>
    </div>
    <div class="w-full absolute top-0">
      <ul role="list" class="divide-y divide-gray-200 dark:divide-gray-700">
        <li class="py-3 sm:py-4">
          <div class="flex items-center px-5">
            <div class="flex-shrink-0">
              <img class="w-12 h-12 rounded-full"
                src="https://as2.ftcdn.net/v2/jpg/05/05/67/65/1000_F_505676530_npWlLUFTryYvGvYs5aNzLrakMvYie6eh.jpg"
                alt="Neil image">
            </div>
            <div class="flex-1 min-w-0 ms-4">
              <p class="text-lg font-medium text-gray-900 truncate dark:text-white">
                Dragon Ball Z
              </p>
              <p class="text-base font-medium text-gray-700 dark:text-gray-400">
                @dbz.tshirts
              </p>
            </div>

          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>

const video = ref(null);
const videoProgress = ref(0);

const updateVideoProgress = () => {
  console.log("I got invocked");
  if (video.value) {
    const videoPlayer = video.value;
    videoProgress.value = ((videoPlayer.currentTime / videoPlayer.duration) * 100).toFixed(10);
  }
}

const toggel = () => {
  if (video.value.paused) {
    video.value.play();
  } else {
    video.value.pause();
  }
}
</script>

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

.ani {
  transition: width 0.3s ease-in-out;
}
</style>