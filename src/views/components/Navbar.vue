<template>
    <nav role="navigation">
        <div class="w-100 border-b border-t border-gray-300 shadow-sm bg-white">
            <div class="container mx-auto">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                    <div class="relative flex items-center justify-between h-20">
                        <div class="lg:flex-auto  flex items-center justify-center sm:items-stretch sm:justify-start">
                          <div class="flex-shrink-0 items-center">
                               <router-link class="no-underline"  to="/">
                                    <img class="block h-12 w-auto hide" src="@/assets/images/navbar_logo_2.svg" alt="CoinFlask Logo" />
                                    <img class="block h-12 w-auto unhide" src="@/assets/images/navbar_logo_sm.png" alt="CoinFlask Logo" />
                               </router-link>
                          </div>
                        </div>


                        <div class="flex-0 text-right justify-end px-2 mt-0">
                            <a href="https://www.linkedin.com/in/dominic-mazzola-3833a686/" target="_blank">
                                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24"><path fill="#2a4365" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                            </a>
                        </div>


                        <!-- <div class="flex-0 text-right justify-end px-2 mt-0">
                            <a href="https://twitter.com/jukabo_NFT" target="_blank">
                                <svg aria-hidden="true"
                                width="36" height="36"
                                focusable="false"
                                data-prefix="fab"
                                  data-icon="twitter"
                                  class="block mx-auto mb-1 pt-1"
                                  role="img"
                                  xmlns="http://www.w3.org/2000/svg"
                                  viewBox="0 0 512 512"
                                >
                                  <path
                                    fill="#2a4365"
                                    d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"
                                  ></path>
                                </svg>
                            </a>
                        </div> -->

                        <div class="flex-0 text-right justify-end px-2 mt-2">
                            <a href="https://github.com/Zalkota" target="_blank">
                                <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 30 30"><path fill="#2a4365" d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                            </a>
                        </div>


                        <!-- <div class="flex-0 text-right w-96 justify-end">
                                <SearchBar ref="searchBar"/>
                         </div> -->
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>


<script>
import UpperNav from './UpperNav.vue';
import SocialRow from './SocialRow.vue';
import SearchBar from './SearchBar.vue';
export default {
  name: 'Navbar',
  props: ["marketData", "totalMarketCap", "totalVolume"],
  components: {UpperNav, SearchBar, SocialRow},
}
</script>
