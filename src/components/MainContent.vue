<template>
	<div class="flex flex-col px-5 md:pl-0 md:pb-6 md:pr-6">
		<div class="md:block flex items-center sticky top-0 z-50 bg-main md:py-6">
			<div class="flex flex-col justify-center items-start h-20 cursor-pointer w-full md:hidden md:pb-1">
			  <svg width="35" height="35" viewBox="0 0 300 300" fill="none" xmlns="http://www.w3.org/2000/svg">
			    <path d="M85 68.9675L99.5481 68.9675L157.882 188.709L142.5 188.709L85 68.9675Z" fill="#2bebc8" />
			    <path d="M201.77 67.8492L215.5 67.8492L157.5 189.155L142.5 189.155L201.77 67.8492Z" fill="#2bebc8" />
			    <path d="M181 112.655H193V237.655H181V112.655Z" fill="#2bebc8" />
			    <path d="M108 112.655H121V237.655H108V112.655Z" fill="#2bebc8" />
			    <path fill-rule="evenodd" clip-rule="evenodd" d="M150 288C226.215 288 288 226.215 288 150C288 73.7847 226.215 12 150 12C73.7847 12 12 73.7847 12 150C12 226.215 73.7847 288 150 288ZM150 300C232.843 300 300 232.843 300 150C300 67.1573 232.843 0 150 0C67.1573 0 0 67.1573 0 150C0 232.843 67.1573 300 150 300Z" fill="#2bebc8" />
			  </svg>
			</div>
      <span class="hidden md:block font-cinzel text-3xl font-bold text-white">MangaVUE</span>
    </div>
    <router-view class="mb-24 mt-2 md:mb-2 md:mt-12" />
	</div>
</template>

<script>
	export default {};
</script>
