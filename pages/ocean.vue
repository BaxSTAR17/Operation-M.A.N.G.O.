<script setup>
    const text1 = ref('')
    const text2 = ref('')
    const text3 = ref('')
    const passkey = ref('')
</script>

<template>
    <main class="w-screen h-screen flex justify-start items-center flex-col border-box gap-5 pt-10 pb-10 overflow-y-auto">
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content m-5 text-center max-w-300 bg-slate-300 justify-center">
            <span class="text-4xl text-black font-bold">OCEAN</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">JOURNEY DEEP BELOW</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-70 h-full rounded-lg" src="../public/img/titanic.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-2xl">In the future, submersibles and other underwater vehicles will eventually succeed in conquering the depths below the ocean to discover new fishes and treasures beneath the vast waters!</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">What ship is famous for sinking? (Starts with T)</span>
            <input type="text" v-model="text1" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text1 === 'Titanic' || text1 == 'titanic'">
                <UTooltip text="R">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">R</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">CORAL REEFS PRESENT!</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-50 h-full rounded-lg" src="../public/img/corals.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">Coral reefs have a bright future ahead as various technologies have been created to strengthen and improve these coral structures, essentially enhancing the habitat of the marine life</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">The main animal of the oceans (Starts with an F)</span>
            <input type="text" v-model="text2" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text2 === 'Fish' || text2 == 'fish'">
                <UTooltip text="E">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">E</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">FULL SHIP UPGRADE</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center bg-slate-400 justify-center">
            <img class="w-100 h-full rounded-lg hidden lg:block" src="../public/img/boat.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-3xl">Ships will be upgraded with technology advancements to improve the passenger experience, like decreasing the swaying or keeling from rocky waves, and improving safety measures to avoid accidents and mishaps
            </span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">A tool used to steer a boat through rowing (Starts with O)</span>
            <input type="text" v-model="text3" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text3 === 'Oar' || text3 == 'oar'">
                <UTooltip text="S">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">S</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-900 justify-start items-center min-h-55">
            <span class="text-white">Enter Passcode</span>
            <input type="text" v-model="passkey" class="rounded-lg w-20 font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="passkey === 'RES' || passkey == 'res'">
                <NuxtLink :to="`/mango/${5}`">
                    <div class="cursor-pointer w-content border-box pl-3 pr-3 shadow-md hover:shadow-xl text-shadow-md text-shadow-cyan-500 hover:text-shadow-lg transition-all ease shadow-cyan-500 min-h-15 bg-cyan-800 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">RES</div>
                </NuxtLink>
            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        background-size: cover;
        background-position: center center;
        background-image: url(../public/img/oceanbg.gif)
    }
</style>