<template>


    <footer class="text-center lg:text-left bg-gray-800 text-gray-500 no-underline border-t-4 border-blue-400">
        <div class="container mx-auto ">
            <div class="mx-6 py-10 text-center md:text-left">
              <div class="grid grid-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                  <h6 class="text-blue-400 uppercase font-semibold mb-4 flex justify-center md:justify-start tracking-wider" style="font-family: Russo One;">
                      Links
                  </h6>
                  <p class="mb-4">
                    <a href="https://www.linkedin.com/in/dominic-mazzola-3833a686/" target="_blank" class="text-gray-300 text-sm font-medium no-underline">Linkedin</a>
                  </p>
                  <p class="mb-4">
                    <a href="https://github.com/Zalkota" target="_blank" class="text-gray-300 text-sm font-medium no-underline">Github</a>
                  </p>
                  <p class="mb-4">
                    <a href="https://twitter.com/jukabo_NFT" target="_blank" class="text-gray-300 text-sm font-medium no-underline">Twitter</a>
                  </p>
                  <p class="mb-4">
                    <a href="https://t.me/Dommazzola" target="_blank" class="text-gray-300 text-sm font-medium no-underline">Telegram</a>
                  </p>
                </div>
                <div>
                  <h6 class="uppercase font-semibold mb-4 flex justify-center md:justify-start text-blue-400 tracking-wider" style="font-family: Russo One;" >
                    Personal Favorites
                  </h6>
                  <p class="mb-4">
                    <a href="https://xcopy.art/" target="_blank" class="text-gray-300 text-sm font-medium no-underline">NFT Artist</a>
                  </p>
                  <p class="mb-4">
                    <a href="https://youtu.be/DGIjuVbGP_A" target="_blank" class="text-gray-300 text-sm font-medium no-underline">Self Development</a>
                  </p>
                  <p class="">
                    <a href="https://www.youtube.com/watch?v=TDGq4aeevgY" target="_blank" class="text-gray-300 text-sm font-medium no-underline">Vitalik Buterin</a>
                  </p>

                </div>
                <div>

                </div>
                <div>
                  <h6 class="
                      uppercase
                      font-semibold
                      text-blue-400
                      tracking-wider
                      mb-4
                      flex
                      items-center
                      justify-center
                      md:justify-start
                    " style="font-family: Russo One;">
                    Portfolio
                  </h6>
                  <p class="text-gray-400 font-medium no-underline text-sm">
                    This portfolio was built using Javascript, VueJS, Tailwind, CSS, HTML5, and Nginx; The website is hosted on a secure Linux Digital Ocean droplet.
                  </p>
                </div>
              </div>
            </div>


            <div class="flex justify-center items-center lg:justify-between p-6 border-t border-gray-700">
              <div class="mr-12 hidden lg:block text-md text-gray-500 font-medium no-underline text-sm">
                <span>Developed by <span class="">Dominic Mazzola</span> </span>
              </div>

              <SocialRow/>

            </div>
        </div>
      </footer>

</template>
<script>
import SocialRow from './SocialRow.vue';
export default {
  name: 'Footer',
  props: [],
  components: {SocialRow},
}
</script>
