<template>
<div id="PromiseCard">
    <div class="flex px-12 pt-20 flex-wrap -m-4">
        <div class="p-4 md:w-1/3">
            <div class="h-full border-2 bg-white border-gray-200 rounded-lg overflow-hidden">
                <img class="lg:h-48 md:h-36 w-full object-cover object-center" src="https://romelakimseva.files.wordpress.com/2018/06/00254ae5-813f-4125-bfe4-412362090c19.jpeg" alt="blog">
                <div class="p-6">
                    <h2 class="tracking-widest text-xs title-font font-medium text-gray-500 mb-1">#{{ promise.category }}</h2>
                    <p class="leading-relaxed mb-3">For I know the thoughts that I think toward you, says the Lord, thoughts of peace and not of evil, to give you a future and a hope..</p>
                    <div class="flex items-center flex-wrap ">
                        <a class="text-indigo-500 inline-flex items-center md:mb-2 lg:mb-0">{{ jsonData.Verse }}
                            <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M5 12h14"></path>
                                <path d="M12 5l7 7-7 7"></path>
                            </svg>
                        </a>
                        <span class="text-gray-600 mr-3 inline-flex items-center lg:ml-auto md:ml-0 ml-auto leading-none text-sm pr-3 py-1">
                            <svg class="w-4 h-4 mr-1" color="red" stroke="currentColor" stroke-width="2" fill="currentColor" stroke-linecap="round" stroke-linejoin="round" viewBox="0 0 24 24">
                                <path fill-rule="evenodd" d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z" clip-rule="evenodd"></path>
                                <circle cx="12" cy="12" r="3"></circle>
                            </svg>1.2K
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>

new Vue({
  el: '#PromiseCard',
  data () {
    return {
      info: null
    }
  },
  mounted () {
    axios
      .get('https://superagency-js.imfast.io/promise/promise.json')
      .then(response => (this.info = response))
      .catch(error => console.log(error))
  }
})
</script>
