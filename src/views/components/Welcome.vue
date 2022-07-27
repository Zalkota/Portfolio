<template>

    <div class="">
        <div class="flex flex-col md:flex-row border border-gray-300 mt-6 mx-auto p-6 rounded-md shadow-md bg-white mb-64">
            <div class="flex-auto">
                <div class="px-6">
                    <img class="block w-48 mt-6 mx-auto" src="@/assets/images/dominic_image.png" alt="Profile Image" />
                </div>
                <div class="px-6 py-2 sm:mt-8">
                    <button class="button w-full text-center bg-white border-2 border-blue-400 hover:bg-blue-400 hover:text-white hover:shadow-md text-blue-400 font-bold py-2 px-6 md:mt-0 mt-4 rounded text-white no-underline" href="https://t.me/Dommazzola" target="_blank">
                        Message
                    </button>
                </div>
            </div>
            <div class="flex-auto mb-4 px-6">
                <div class="md:flex">
                    <div class="md:flex-0 text-center ">
                        <h1 class="text-gray-900 font-bold text-xl lg:text-2xl mb-1" style="font-family: Russo One;">
                            Dominic Mazzola
                        </h1>
                    </div>
                    <div class="flex-auto hide">
                        <svg class="w-8 mt-3 mx-3" viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg"><path d="m16.1 48.5c-.5-.1-.9-.2-1.4-.4s-.9-.3-1.3-.5c-.9-.4-1.7-.9-2.5-1.5-1.6-1.1-2.9-2.6-3.9-4.4-1-1.7-1.6-3.7-1.7-5.6-.1-1 0-1.9.1-2.9.1-.5.2-.9.3-1.4s.3-.9.4-1.4l.1 1.4c0 .5.1.9.2 1.4.1.9.3 1.8.5 2.6.4 1.7 1 3.3 1.9 4.8s1.9 2.9 3.2 4.2c.6.6 1.3 1.2 2 1.8.3.3.7.6 1.1.9zm-.3 3.6c-.3.2-.7.3-1.1.4s-.7.2-1.1.2c-.7.1-1.5.2-2.3.1-1.5-.1-3.1-.5-4.4-1.2-1.4-.7-2.6-1.8-3.4-3.1-.4-.6-.8-1.3-1.1-2-.1-.3-.2-.7-.3-1.1 0-.3-.1-.6-.1-1 .3.3.5.6.7.8.3.3.5.6.7.8.5.5.9 1 1.4 1.4 1 .9 2 1.7 3.2 2.3 1.1.6 2.4 1.1 3.6 1.5.6.2 1.3.3 2 .5.3.1.7.1 1 .2.5.1.8.1 1.2.2m22.6-48.6c.5.1.9.3 1.4.5s.9.4 1.3.6c.9.5 1.7 1 2.5 1.6 1.6 1.2 2.9 2.8 3.8 4.6s1.4 3.8 1.4 5.7c0 1-.1 1.9-.3 2.9-.1.5-.2.9-.4 1.4s-.3.9-.5 1.3l-.1-1.4c0-.5 0-.9-.1-1.4l-.3-2.7c-.3-1.7-.9-3.4-1.7-5s-1.8-3-3-4.3c-.6-.7-1.3-1.3-1.9-2-.3-.3-.7-.6-1.1-.9zm8.7-.4c.4.1.7.2 1 .4.3.1.7.3 1 .5.6.4 1.2.8 1.8 1.3 1.1 1 2 2.2 2.5 3.6.6 1.4.8 2.9.6 4.4-.1.7-.3 1.4-.5 2.1-.1.3-.3.7-.4 1-.2.3-.3.6-.6.9v-1-1c0-.7-.1-1.3-.1-1.9-.2-1.3-.4-2.5-.9-3.6-.5-1.2-1.1-2.2-1.8-3.3-.4-.5-.8-1.1-1.2-1.6-.2-.3-.4-.5-.7-.8-.2-.5-.5-.8-.7-1" fill="#42ade2"/><path d="m10 18c-2 .9-2.7 3.3-1.8 5.3l12.6 26.3 7-3.3-12.6-26.4c-.9-2-3.2-2.9-5.2-1.9m33.1 20.9 7.4-3.5-14.4-30c-1-2-3.4-2.9-5.5-1.9-2 1-2.9 3.4-1.9 5.5z" fill="#ffdd67"/><path d="m30.7 3.4c-.2.1-.4.2-.6.4 1.9-.5 3.9.4 4.8 2.2l14.4 30 1.3-.6-14.4-30c-1-2.1-3.4-3-5.5-2" fill="#eba352"/><path d="m27.8 46.2 7.7-3.7-14.7-30.6c-1-2.1-3.6-3.1-5.7-2.1s-3 3.6-2 5.7z" fill="#ffdd67"/><path d="m15.1 9.9c-.2.1-.4.2-.6.4 1.9-.5 4.1.4 5 2.3l9.1 19.1 2.2 1.3-10-21c-1-2.2-3.5-3.1-5.7-2.1" fill="#eba352"/><path d="m34.3 40.1 7.7-3.7-14.7-30.6c-1-2.1-3.6-3.1-5.7-2-2.1 1-3 3.6-2 5.7z" fill="#ffdd67"/><path d="m21.6 3.7c-.2.1-.4.3-.6.4 1.9-.5 4.1.4 5 2.3l10.3 21.6 2.2 1.3-11.2-23.5c-1-2.2-3.6-3.1-5.7-2.1m-11.6 14.3c-.2.1-.4.2-.6.4 1.8-.5 3.7.4 4.5 2.2l7.5 15.7 2.2 1.3-8.4-17.6c-.9-2.1-3.2-3-5.2-2" fill="#eba352"/><path d="m60.8 15c-2.7-2.1-7.1.2-9.3 7.4-1.5 5-1.7 6.5-4.9 8l-1.8-3.7s-28.4 13.7-27.3 15.9c0 0 3.4 10.6 9.2 15.5 8.6 7.4 28.7-.5 29.6-19.6.5-11.1 7.4-21.2 4.5-23.5" fill="#ffdd67"/><g fill="#eba352"><path d="m60.8 15c-.5-.4-1.1-.6-1.7-.7.1.1.3.1.4.2 3 2.3-.1 7.6-1.8 12.4-1.4 3.8-2.6 7.7-2.4 11.5.8 16.6-15.9 24.5-25.9 21.5 9.8 4.1 28-3.7 27.2-21-.2-3.8.9-7.5 2.4-11.5 1.6-4.8 4.7-10.1 1.8-12.4"/><path d="m47.5 30c-6.2.7-15.3 9.6-8.9 19.3-4.7-9.8 3-16.4 7.9-18.7.5-.4 1-.6 1-.6"/></g></svg>
                    </div>
                </div>
                <div class="text-center md:text-left">
                    <h2 class="text-gray-700 font-thin text-sm ">Forward-looking Engineer with five years of experience creating full stack software application with a burning passion for decentralized technologies (Web3, NFTs, metaverse, etc.). I'm very self-driven, work well in teams, communicate effectively, persistent at solving problems, and I believe everyone has a passion whether out not they've found it yet.</h2>
                    <h3 class="font-bold text-xl mb-0 mt-6">Favorite Quote</h3>
                </div>
                <div class="p-4 rounded-lg my-3 bg-blue-100 text-blue-700">
                    <p class=""><span class="italic">"Don't judge each day by the harvest you reap but by the seeds that you plant."</span> -Robert Louis Stevenson</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

export default {
  name: 'Welcome',
  props: [],

    methods: {

      }
    }
</script>
