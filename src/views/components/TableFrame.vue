<template>
        <div class="container mx-auto mt-2 lg:mt-16 mb-12 lg:mb-32  px-4 sm:px-6 lg:px-10">


            <t-modal
              header="Title of the modal"
            >
              Content of the modal.
              <template v-slot:footer>
                <div class="flex justify-between">
                  <t-button type="button">
                    Cancel
                  </t-button>
                  <t-button type="button">
                    Ok
                  </t-button>
                </div>
              </template>
            </t-modal>

        <div class="flex flex-wrap">
            <div class="w-full">
                <ul v-show="this.$route.name == 'home'" class="flex mb-0 list-none flex-wrap pt-3 flex-row border-b border-gray-300">
                <li class=" mr-2 last:mr-0 flex-1 md:flex-initial text-center">
                  <a class="text-sm text-gray-600 font-bold px-5 py-3 block leading-normal no-underline cursor-pointer" v-on:click="toggleTabs(0)" v-bind:class="{'border-none': openTab !== 0, 'border-b-2 border-blue-500 bg-gray-100 text-blue-500': openTab === 0}">
                    Welcome
                  </a>
                </li>
                <li class=" mr-2 last:mr-0 flex-1 md:flex-initial text-center">
                  <a class="text-sm text-gray-600 font-bold px-5 py-3 block leading-normal no-underline cursor-pointer" v-on:click="toggleTabs(2)" v-bind:class="{'border-none': openTab !== 2, 'border-b-2 border-blue-500 bg-gray-100 text-blue-500': openTab === 2}">
                    Résumé
                  </a>
                </li>
                <li class=" mr-2 last:mr-0 flex-1 md:flex-initial text-center">
                  <a class="text-sm text-gray-600 font-bold px-5 py-3 block leading-normal no-underline cursor-pointer" v-on:click="toggleTabs(1)" v-bind:class="{'border-none': openTab !== 1, 'border-b-2 border-blue-500 bg-gray-100 text-blue-500': openTab === 1}">
                    Portfolio
                  </a>
                </li>
                <!-- <li class="-mb-px mr-2 last:mr-0 flex-0 text-center">
                  <a class="text-sm text-gray-600 font-bold px-6 py-3 pl-2 block leading-normal no-underline cursor-pointer" v-on:click="toggleTabs(3)" v-bind:class="{'border-none': openTab !== 3, 'border-b-2 border-blue-500 text-blue-500': openTab === 3}">
                     <img class="inline-block h-6 w-auto" src="@/assets/images/icon-star-active.svg" alt="CoinFlask Logo" />
                    Favorites
                  </a>
                </li>
                <li class="-mb-px mr-2 last:mr-0 flex-0 text-center">
                  <a class="text-sm text-gray-600 font-bold px-6 py-3 pl-2 block leading-normal no-underline cursor-pointer" v-on:click="toggleTabs(3)" v-bind:class="{'border-none': openTab !== 3, 'border-b-2 border-blue-500 text-blue-500': openTab === 3}">
                    NFT Gallery
                  </a>
                </li> -->
              </ul>


              <!-- <button v-on:click="getFavoritesData()" name="button"> {{ getFavoritesData.id }}</button> -->
              <div class="relative flex flex-col min-w-0 break-words w-full">
                <div class="flex-auto">
                  <div v-show="this.$route.name == 'home'" class="tab-content tab-space">
                    <div v-bind:class="{'hidden': openTab !== 1, 'block': openTab === 1}">

                        <div class="flex  mb-2 mx-auto py-4 ">
                            <div class="flex-1">
                                 <h1 class="text-gray-900 font-bold text-xl lg:text-2xl mb-1" style="font-family: Russo One;">Personal Projects Developed by Dominic</h1>
                                 <h2 class="text-gray-600 font-thin text-sm">Feel free to reach out to me if you have any questions.</h2>
                            </div>
                        </div>

                         <div class="mx-auto grid lg:grid-cols-4 lg:gap-4 md:grid-cols-2 md:gap-2 text-left w-full">

                             <template v-for="card in portfolio">
                                 <Card
                                 :id="card.id"
                                 :title="card.title"
                                 :description="card.description"
                                 :imageURL="card.imageURL"
                                 :tags="card.tags"
                                 v-bind:detail_view_card="card.detail_pdf_array"
                                 :websiteURL="card.websiteURL"
                                 :githubURL="card.githubURL"
                                 :etherscanURL="card.etherscanURL"
                                 :privateRepo="card.privateRepo"
                                 />
                             </template>

                          </div>

                    </div>
                    <div v-bind:class="{'hidden': openTab !== 2, 'block': openTab === 2}">
                        <Resume />
                    </div>

                    <div v-bind:class="{'hidden': openTab !== 0, 'block': openTab === 0}">
                        <Welcome />
                    </div>

                  </div>

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>

import CoinGecko from 'coingecko-api'
const coinGeckoClient = new CoinGecko();
import Card from "./Card.vue";
import Resume from "./Resume.vue";
import Welcome from "./Welcome.vue";
import portfolioJson from "../../assets/portfolio.json";

export default {
  name: 'TableFrame',
  props: [],
  components: {Card, Resume, Welcome},
  data() {
    return {
         openTab: 0,
         alwaysTrue: true,
         alwaysFalse: false,
         tableData: [],
         portfolio: portfolioJson,
    }
  },
  computed: {
      favoriteArray() {
          return this.$store.getters.getStoredfavoriteArray;
      },

  },

  methods: {

      readFavoriteToggleEvent(payload) {
          let id = payload.id
          this.toggleFavorite(id)
          console.log("readFavoriteToggleEvent", id)
      },


     toggleFavorite(id) {
         let position = this.favoriteMarketData.map((element) => element.id).indexOf(id)
         console.log("position", position)

         // check is id is already found in favoriteMarketData
         if (position > -1) {
             // Object already in favorites
             // remove it
             this.favoriteMarketData.splice(position, 1);
             this.$store.commit('setFavoriteMarketData', this.favoriteMarketData)
             // console.log("Favorite removed", id, "from", this.favoriteMarketData)

         } else {
             // Object not found in favorites
             // obtain market data for that favorite
             let marketDataQuery = this.marketData.filter(x => x.id.toLowerCase() == id)
             // add it to the favoriteMarketData array
             this.favoriteMarketData.push(marketDataQuery[0])
             this.$store.commit('setFavoriteMarketData', this.favoriteMarketData)
             // console.log("Favorite added", id, "to", this.favoriteMarketData)

         }
     },

    toggleTabs: function(tabNumber){
        this.openTab = tabNumber
    }
  }
}
</script>
