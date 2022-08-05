<template>

    <div class="">
        <div class="flex border bg-white border-gray-300 mt-6 mx-auto px-6 rounded-md shadow-sm  hide">
            <div class="flex-auto mb-4">
                <h1 class="text-gray-900 font-bold text-xl lg:text-2xl mb-1" style="font-family: Russo One;">Download Resume PDF</h1>
                <h2 class="text-gray-700 font-thin text-sm ">View Dominic's resume below or download it in PDF format.</h2>
            </div>
            <div class="flex-1 m-6 text-right">
                <a class="bg-blue-400 hover:bg-blue-500 hover:shadow-md text-white font-bold py-2 px-4 rounded inline-flex items-center text-white no-underline" :href="LinkToPDF()" target="_blank">
                    <svg class="w-4 h-4 mr-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path fill="#fff" d="M13 8V2H7v6H2l8 8 8-8h-5zM0 18h20v2H0v-2z"/></svg>
                    View as PDF
                </a>
            </div>

        </div>

        <div class="w-full mt-6 text-right">
            <a class="unhide bg-blue-400 hover:bg-blue-500 hover:shadow-md text-white font-bold py-2 px-4 rounded inline-flex items-center text-white no-underline" :href="LinkToPDF()" target="_blank">
                View as PDF
            </a>
        </div>

        <div class=" text-left m-6 border-gray-300 hover:shadow-md border ">
            <pdf src="resume.pdf"></pdf>
        </div>
        
        <div  class=" text-left m-6 border-gray-300 hover:shadow-md border">
            <pdf src="resume_2.pdf"></pdf>
        </div>
    </div>

</template>
<script>


export default {
  name: 'Resume',
  props: [],
  data() {
    return {
         URL: "https://dominics-portfolio-media.s3.amazonaws.com/Resume_Dominic_Mazzola_0728-2.pdf"
    }
  },
  methods: {
     LinkToPDF() {
         return this.URL
     }
  }

  }



</script>
