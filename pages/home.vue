<template>
  <Nav />
  <div class="bg-black text-white text-xl p-10 justify-center sm:px-60 sm:py-40 sm:text-6xl">
    <span>Comet helps global brands launch shopping journeys </span>
    <span>that are unique to the needs of each touch point </span>
  </div> 
  <div class="bg-black h-full flex flex-wrap-reverse sm:flex-nowrap">
    <div class="w-full py-10 mx-10 px-10 relative border sm:w-3/5">
      <div class="absolute flex text-white bg-black border-text text-xl">
        <span class="p-1.5">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-gear-fill"
            viewBox="0 0 16 16"
          >
            <path
              d="M9.405 1.05c-.413-1.4-2.397-1.4-2.81 0l-.1.34a1.464 1.464 0 0 1-2.105.872l-.31-.17c-1.283-.698-2.686.705-1.987 1.987l.169.311c.446.82.023 1.841-.872 2.105l-.34.1c-1.4.413-1.4 2.397 0 2.81l.34.1a1.464 1.464 0 0 1 .872 2.105l-.17.31c-.698 1.283.705 2.686 1.987 1.987l.311-.169a1.464 1.464 0 0 1 2.105.872l.1.34c.413 1.4 2.397 1.4 2.81 0l.1-.34a1.464 1.464 0 0 1 2.105-.872l.31.17c1.283.698 2.686-.705 1.987-1.987l-.169-.311a1.464 1.464 0 0 1 .872-2.105l.34-.1c1.4-.413 1.4-2.397 0-2.81l-.34-.1a1.464 1.464 0 0 1-.872-2.105l.17-.31c.698-1.283-.705-2.686-1.987-1.987l-.311.169a1.464 1.464 0 0 1-2.105-.872zM8 10.93a2.929 2.929 0 1 1 0-5.86 2.929 2.929 0 0 1 0 5.858z"
            />
          </svg>
        </span>
        <span class="full-grad">
          Comet aggregates your data & creates stores which your customers can
          interact with
        </span>
      </div>
      <masonry-wall
        :items="items"
        :ssr-columns="4"
        :max-columns="3"
        :column-width="240"
        :gap="15"
      >
        <template #default="{ item, index }">
          <ClientDataCard
            :imgWidth="getRandomNumber(300, 300)"
            :imgHeight="getRandomNumber(100, 200)"
            :item="item"
          />
        </template>
      </masonry-wall>
    </div>
    <div class="w-full p-10 sm:w-2/5">
      <Shop />
    </div>
  </div>
</template>

<script setup>
  const items = [
    {
      title: "First",
      description: "The first item.",
      fullImage: true,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "First",
      description: "The first item.",
      fullImage: false,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "First",
      description: "The first item.",
      fullImage: true,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "First",
      description: "The first item.",
      fullImage: true,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
    {
      title: "Second",
      description: "The second item.",
      fullImage: false,
    },
  ];

  const getRandomNumber = (min, max) => {
    return Math.ceil(Math.random() * (max - min) + min);
  };
</script>
<style scoped>
  .border-text {
    top: -35px;
    background-color: black;
    padding: 20px 15px;
  }
</style>
