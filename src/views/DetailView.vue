<template>
    <div>
        <Navbar/>
        <div class="container mx-auto mt-2 lg:mt-16 mb-12 lg:mb-32  px-4 sm:px-6 lg:px-10e">
            <div class="flex flex-col lg:flex-row border border-gray-300 mt-6 mx-auto rounded-md bg-white shadow-md">
                <div class="flex-1 mb-4 text-center lg:text-left">
                    <div class="flex border-b border-gray-300 p-6">
                        <div class="flex-1">
                            <h1 class="text-gray-900 font-bold text-4xl lg:text-4xl mb-0 mt-0 " style="font-family: Russo One;">{{ getObject.title }}</h1>
                            <span class="text-gray-700 text-sm">{{ getObject.location }}</span>
                        </div>
                        <div class="flex-1 text-right">
                            <a class="bg-white border border-blue-400 hover:bg-blue-500 hover:shadow-md text-blue-400 font-bold mt-1 lg:mr-4 py-3 px-4 rounded inline-flex items-center text-white no-underline" :href="getObject.githubURL" target="_blank">
                                Website
                            </a>
                            <a class="bg-blue-400 hover:bg-blue-500 hover:shadow-md text-white font-bold mt-1 py-3 px-4 rounded inline-flex items-center text-white no-underline" :href="getObject.githubURL" target="_blank">
                                <svg class="w-6 h-6 mr-2" xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 30 30"><path fill="#fff" d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                                Github Repo
                            </a>
                        </div>
                    </div>
                    <div class="p-4">
                        <h2 class="text-gray-700 font-thin text-sm">{{ getObject.description}}</h2>
                        <br>
                        <h3 class="text-gray-700 font-thin text-sm">Below are screenshots of the web application when it was in production. <br>All of the code is available in the Github repositroy.</h3>
                    </div>
                </div>

        </div>
        <div class="mx-auto text-left w-full m-6 border-gray-300 hover:shadow-md border ">
            <pdf src="resume.pdf"></pdf>
        </div>
        <!-- <div v-for="object in getDetailPDFArray" class="mx-auto text-left w-full m-6 border-gray-300 hover:shadow-md border ">
            <pdf src="resume.pdf"></pdf>
            {{ getDocumentURL(object) }}
        </div> -->

        </div>
        <Footer/>
    </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
import portfolioJson from "../assets/portfolio.json";

export default {
  name: "Home",
  data() {
    return {
         portfolio: portfolioJson,
    }
  },
  components: { Navbar, Footer},

  methods: {
      getDocumentURL(object) {
          return object + '.pdf'
      }
  },
  computed: {
      getDetailPDFArray() {
          return this.portfolio[this.$route.params.projectId].detail_pdf_array
      },

      getObject() {
          return this.portfolio[this.$route.params.projectId]
      },


  }
};
</script>
