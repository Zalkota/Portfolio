<template>
    <div class="flex-1 w-full bg-white rounded-lg overflow-hidden flex flex-col justify-center border border-gray-400 hover:shadow-md mb-6 md:mb-0">
        <!-- <router-link v-bind:to="getLinkUrl(id)" class=" cursor-pointer  no-underline select-none inline-block  relative"> -->
            <img class="object-center object-cover h-auto w-full" :src="getImgUrl(imageURL)" alt=""/>
            <div class="text-left px-6 sm:px-4  pt-4 sm:py-4 sm:pb-4 ">
               <h4 class="text-2xl md:text-lg text-gray-800 font-bold mb-2">{{ title }}</h4>
               <p class="text-gray-700 text-xs font-medium">{{ truncateDescription(description) }}</p>
            </div>
            <div class="px-6 sm:px-4 py-4 sm:pt-2">
                <template v-for="tag in tags">
                    <span class="text-xs font-medium inline-block py-1 px-3 rounded-xl text-gray-800 bg-gray-300 last:mr-0 mr-1 hover:bg-blue-300">
                      {{ tag }}
                    </span>
                </template>
            </div>
            <!-- </router-link> -->
            <div class="flex p-6 md:p-3 py-3 bg-gray-100">
                <div v-if="!privateRepo == true" class="text-right flex-0 justify-end px-2">
                    <a v-bind:href="githubURL" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" viewBox="0 0 30 30"><path fill="#2a4365" d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                    </a>
                </div>
                <div v-if="privateRepo == true" class="text-right flex-0 justify-end px-2">
                    <a v-bind:href="githubURL" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24"><path fill="#F56565" d="M12 2c5.514 0 10 4.486 10 10s-4.486 10-10 10-10-4.486-10-10 4.486-10 10-10zm0-2c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm4 17h-8v-6h8v6zm-6-6v-2c0-1.104.897-2 2-2s2 .896 2 2v2h1v-2c0-1.656-1.343-3-3-3s-3 1.344-3 3v2h1z"/></svg>
                    </a>
                </div>
            </div>
    </div>
</template>
<script>



export default {
    name: 'Card',
    props: ['id', 'title',  'description', 'imageURL', 'tags', 'githubURL', 'privateRepo'],

    methods: {

        getImgUrl(imageURL) {
            var images = require.context('@/assets/images/cards/', false, /\.jpg$/)
            return images('./' + imageURL + ".jpg")
        },

        getLinkUrl(id){
            return `/project/${id}`
        },

        truncateDescription(payload) {
            let maxLength = 150
            if(payload.length >= maxLength) {
                let trimmedString = payload.substring(0, maxLength) ;
                trimmedString = trimmedString.substr(0, Math.min(trimmedString.length, trimmedString.lastIndexOf(" ")))
                return trimmedString + '...'
            } return payload

        }
    }
}
</script>
