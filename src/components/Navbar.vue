<template>
  <!-- <nav class="bg-main px-6 flex flex-col justify-center h-screen sticky top-0"> -->
  <nav class="bg-main md:px-3 md:flex md:flex-col md:flex-none md:justify-center md:items-center md:h-screen md:sticky md:top-0">
    <div>
      <ul>
        <li class="hidden md:block absolute top-0">
          <div class="flex flex-col justify-center items-center h-20 pb-1 cursor-pointer w-16">
            <svg width="35" height="35" viewBox="0 0 300 300" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M85 68.9675L99.5481 68.9675L157.882 188.709L142.5 188.709L85 68.9675Z" fill="#2bebc8" />
              <path d="M201.77 67.8492L215.5 67.8492L157.5 189.155L142.5 189.155L201.77 67.8492Z" fill="#2bebc8" />
              <path d="M181 112.655H193V237.655H181V112.655Z" fill="#2bebc8" />
              <path d="M108 112.655H121V237.655H108V112.655Z" fill="#2bebc8" />
              <path fill-rule="evenodd" clip-rule="evenodd" d="M150 288C226.215 288 288 226.215 288 150C288 73.7847 226.215 12 150 12C73.7847 12 12 73.7847 12 150C12 226.215 73.7847 288 150 288ZM150 300C232.843 300 300 232.843 300 150C300 67.1573 232.843 0 150 0C67.1573 0 0 67.1573 0 150C0 232.843 67.1573 300 150 300Z" fill="#2bebc8" />
            </svg>
          </div>
        </li>
        <div class="flex flex-row justify-around items-center md:grid md:grid-cols-1 md:gap-2 px-8 py-2 bg-teriary md:px-2 md:rounded-md">
          <router-link
            :to="{ name: 'manga-lists', params: { page: 1 } }" exact
            class="flex flex-col w-12 h-12 text-white justify-center items-center transition duration-300 ease-id-out rounded-md hover:bg-purple hover:text-white"
            :class="[routeName == 'manga-lists' ? 'bg-purple' : '']">
            <span>
              <Icon name="home" class="fill-current h-5 w-5 transition ease-in-out duration-200" />
            </span>
          </router-link>
          <router-link
            :to="{ name: 'manga-recommended' }" exact
            class="flex flex-col w-12 h-12 text-white justify-center items-center transition duration-300 ease-id-out rounded-md hover:bg-purple hover:text-white":class="[routeName == 'manga-recommended' ? 'bg-purple' : '']">
            <span>
              <Icon name="star" class="fill-current h-5 w-5 transition ease-in-out duration-200" />
            </span>
          </router-link>
          <router-link
            :to="{ name: 'manga-popular', params: { popularity: 'popular', page: 1 } }" exact
            class="flex flex-col w-12 h-12 text-white justify-center items-center transition duration-300 ease-id-out rounded-md hover:bg-purple hover:text-white":class="[routeName == 'manga-popular' ? 'bg-purple' : '']">
            <span>
              <Icon name="trending-up" class="fill-current h-5 w-5 transition ease-in-out duration-200" />
            </span>
          </router-link>
        </div>
      </ul>
    </div>
  </nav>
</template>

<script>
  export default {
    computed: {
      routeName() { return this.$route.name },
    },
  }
</script>