<script setup>
    const text1 = ref('')
    const text2 = ref('')
    const text3 = ref('')
    const passkey = ref('')
</script>

<template>
    <main class="w-screen h-screen flex justify-start items-center flex-col border-box gap-5 pt-10 pb-10 overflow-y-auto">
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content m-5 text-center max-w-300 bg-slate-300 justify-center">
            <span class="text-4xl text-black font-bold">GAMING & ENTERTAINMENT</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">VIRTUAL GAMING</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-70 h-full rounded-lg" src="../public/img/vr.JPG" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-2xl">Players will now be able to immerse themselves inside games as virtual reality games take the scene and will enhance the player's experiences by making them feel actual objects from the game and improving the fun in video games!</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">Pokemon Go. AR or VR?</span>
            <input type="text" v-model="text1" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text1 === 'AR' || text1 == 'ar'">
                <UTooltip text="U">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">U</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">360 CINEMAS</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-50 h-full rounded-lg" src="../public/img/360movie.JPG" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">Movies will make a breakthrough with the birth of 360 movies and 360 theaters, paving the way for a thrilling experience by giving the audience the ability to watch the movie in their surroundings and making an interactive theatrical experience!</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">The main character of the film (Starts with P)</span>
            <input type="text" v-model="text2" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text2 === 'Protagonist' || text2 == 'protagonist'">
                <UTooltip text="T">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">T</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">WIFI STRONG MEANS SERVER STRONG</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center bg-slate-400 justify-center">
            <img class="w-100 h-full rounded-lg hidden lg:block" src="../public/img/wifi.JPG" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-3xl">Wifi, Internet Services and Servers will be improved to enhance the experience of both games (Especially VR) and films without any breaks, and lags along with lesser disconnections and mishaps that may happen along the way
            </span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">stands for world wide web</span>
            <input type="text" v-model="text3" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text3 === 'WWW' || text3 == 'www'">
                <UTooltip text="U">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">U</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-900 justify-start items-center min-h-55">
            <span class="text-white">Enter Passcode</span>
            <input type="text" v-model="passkey" class="rounded-lg w-20 font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="passkey === 'UTU' || passkey == 'utu'">
                <NuxtLink :to="`/mango/${4}`">
                    <div class="cursor-pointer w-content border-box pl-3 pr-3 shadow-md hover:shadow-xl text-shadow-md text-shadow-cyan-500 hover:text-shadow-lg transition-all ease shadow-cyan-500 min-h-15 bg-cyan-800 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">UTU</div>
                </NuxtLink>
            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        background-size: cover;
        background-position: center center;
        background-image: url(../public/img/2017.gif)
    }
</style>