<template>
  <router-link
    :to="{ name: 'manga-details', params: { manga: manga.endpoint } }"
    class="w-full">
    <div
      class="flex flex-col md:flex-row h-full bg-secondary text-white hover:text-green shadow-md rounded-md transform transition duration-300 ease-in-out hover:-translate-y-1 hover:shadow-lg md:max-h-50 lg:max-h-40">
      <img
        :src="thumb"
        :alt="title"
        class="w-full h-40 rounded-t-md object-cover md:rounded-l-md md:rounded-t-none md:w-2/5 md:h-44 lg:h-40"/>
      <div class="absolute items-baseline l-0 m-2">
        <div
          class="flex font-nunito font-semibold text-xs bg-gray-300 rounded-full px-2">
          <Icon name="clock" width="15" class="text-black" />
          <span v-html="updated_on" class="ml-0.5 mt-0.5 text-black"></span>
        </div>
      </div>
      <div class="p-3 md:pt-2 md:px-3">
        <h1 v-html="title" class="font-ptserif text-md mb-1"></h1>
        <span v-html="chapter" class="font-poppins text-white text-xs"></span>
      </div>
    </div>
  </router-link>
</template>

<script>
  export default {
    props: {
      manga: Object,
    },
    computed: {
      thumb() { return this.manga.thumb },
      title() { return this.manga.title },
      chapter() { return this.manga.chapter },
      updated_on() { return this.manga.updated_on + " lalu" },
    },
  };
</script>
