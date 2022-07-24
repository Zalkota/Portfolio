<template>
    <div class="relative flex-1 w-full bg-white rounded-lg overflow-hidden flex flex-col justify-center border border-gray-400 hover:shadow-md mb-6 md:mb-0 pb-12">
        <!-- <router-link v-bind:to="getLinkUrl(id)" class=" cursor-pointer  no-underline select-none inline-block  relative"> -->
            <img class="object-center object-cover h-auto w-full" :src="getImgUrl(imageURL)" alt=""/>
            <div class="text-left px-6 sm:px-4  pt-4 sm:py-4 sm:pb-4 ">
               <!-- <h4 class="text-2xl md:text-lg text-gray-800 font-bold mb-2">{{ title }}</h4> -->
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
            <div class="flex p-6 md:p-3 py-3 bg-gray-100 absolute bottom-0 w-full">
                <div v-if="githubURL != ''" class="text-right flex-0 justify-end px-2">
                    <a v-bind:href="githubURL" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" viewBox="0 0 30 30"><path fill="#4299e1" d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                    </a>
                </div>
                <div v-if="githubURL == ''" class="text-right flex-0 justify-end px-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24"><path fill="#2a4365" d="M12 2c5.514 0 10 4.486 10 10s-4.486 10-10 10-10-4.486-10-10 4.486-10 10-10zm0-2c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm4 17h-8v-6h8v6zm-6-6v-2c0-1.104.897-2 2-2s2 .896 2 2v2h1v-2c0-1.656-1.343-3-3-3s-3 1.344-3 3v2h1z"/></svg>
                </div>
                <div v-if="websiteURL != ''" class="text-right flex-0 justify-end pl-4 md:px-2">
                    <a v-bind:href="websiteURL" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="#4299e1" d="M15 12c0 1.654-1.346 3-3 3s-3-1.346-3-3 1.346-3 3-3 3 1.346 3 3zm9-.449s-4.252 8.449-11.985 8.449c-7.18 0-12.015-8.449-12.015-8.449s4.446-7.551 12.015-7.551c7.694 0 11.985 7.551 11.985 7.551zm-7 .449c0-2.757-2.243-5-5-5s-5 2.243-5 5 2.243 5 5 5 5-2.243 5-5z"/></svg>
                    </a>
                </div>
                <div v-if="websiteURL == ''" class="text-right flex-0 justify-end pl-4 md:px-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="#e2e8f0" d="M11.885 14.988l3.104-3.098.011.11c0 1.654-1.346 3-3 3l-.115-.012zm8.048-8.032l-3.274 3.268c.212.554.341 1.149.341 1.776 0 2.757-2.243 5-5 5-.631 0-1.229-.13-1.785-.344l-2.377 2.372c1.276.588 2.671.972 4.177.972 7.733 0 11.985-8.449 11.985-8.449s-1.415-2.478-4.067-4.595zm1.431-3.536l-18.619 18.58-1.382-1.422 3.455-3.447c-3.022-2.45-4.818-5.58-4.818-5.58s4.446-7.551 12.015-7.551c1.825 0 3.456.426 4.886 1.075l3.081-3.075 1.382 1.42zm-13.751 10.922l1.519-1.515c-.077-.264-.132-.538-.132-.827 0-1.654 1.346-3 3-3 .291 0 .567.055.833.134l1.518-1.515c-.704-.382-1.496-.619-2.351-.619-2.757 0-5 2.243-5 5 0 .852.235 1.641.613 2.342z"/></svg>
                </div>
            </div>
    </div>
</template>
<script>



export default {
    name: 'Card',
    props: ['id', 'title',  'description', 'imageURL', 'tags', 'websiteURL', 'githubURL', 'privateRepo'],

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
