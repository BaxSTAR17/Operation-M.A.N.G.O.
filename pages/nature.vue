<script setup>
    const text1 = ref('')
    const text2 = ref('')
    const text3 = ref('')
    const passkey = ref('')
</script>

<template>
    <main class="w-screen h-screen flex justify-start items-center flex-col border-box gap-5 pt-10 pb-10 overflow-y-auto">
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content m-5 text-center max-w-300 bg-slate-300 justify-center">
            <span class="text-4xl text-black font-bold">NATURE</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">TALKING ANIMALS</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-70 h-full rounded-lg" src="../public/img/DUG.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-2xl">For certain animals, Scientists have found a remarkable discovery to be able to convert animal expressions into speech, essentially paving the way for talking animals which can improve our bonds with wildlife and even our pets. The best example of this is Dug from UP</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">Loud sounds or noise from a dog (Starts with a B)</span>
            <input type="text" v-model="text1" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text1 === 'Bark' || text1 == 'bark'">
                <UTooltip text="L">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">L</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">AGRICULTURE'S ENHANCEMENT</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-50 h-full rounded-lg" src="../public/img/agri.JPG" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">gricultural technology will advance with the help of AI and various technology to potentially speed up agricultural processes and even conduct precautionary measures to improve health and safety like detecting risks of potential sicknesses for various products! </span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">What is a tool, used to cultivate soil? (Starts with H)</span>
            <input type="text" v-model="text2" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text2 === 'Hoe' || text2 == 'hoe'">
                <UTooltip text="D">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">D</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">FOSSILS! RISE!</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center bg-slate-400 justify-center">
            <img class="w-100 h-full rounded-lg hidden lg:block" src="../public/img/fossil.png" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-3xl">As scientists continue to extract DNA from fossils, Ancient animals from prehistoric past may be revived and brought back to life by making hybrids, allowing us to have a glimpse into the past and hopefully welcome it to the future!</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">The T in T-rex (Starts with G)</span>
            <input type="text" v-model="text3" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text3 === 'Tyrannosaurus' || text3 == 'tyrannosaurus'">
                <UTooltip text="F">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">F</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-900 justify-start items-center min-h-55">
            <span class="text-white">Enter Passcode</span>
            <input type="text" v-model="passkey" class="rounded-lg w-20 font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="passkey === 'LDF' || passkey == 'ldf'">
                <NuxtLink :to="`/mango/${3}`">
                    <div class="cursor-pointer w-content border-box pl-3 pr-3 shadow-md hover:shadow-xl text-shadow-md text-shadow-cyan-500 hover:text-shadow-lg transition-all ease shadow-cyan-500 min-h-15 bg-cyan-800 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">LDF</div>
                </NuxtLink>
            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        background-size: cover;
        background-position: center center;
        background-image: url(../public/img/naturebg.gif)
    }
</style>