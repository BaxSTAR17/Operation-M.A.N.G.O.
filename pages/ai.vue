<script setup>
    const text1 = ref('')
    const text2 = ref('')
    const text3 = ref('')
    const passkey = ref('')
</script>

<template>
    <main class="w-screen h-screen flex justify-start items-center flex-col border-box gap-5 pt-10 pb-10 overflow-y-auto">
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content m-5 text-center max-w-300 bg-slate-300 justify-center">
            <span class="text-4xl text-black font-bold">ARTIFICIAL INTELLIGENCE</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">ROBOTS</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-70 h-full rounded-lg" src="../public/img/airobot.png" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">Artificial Intelligence may appear solely through digital products, but it soon takes a physical form! Don't fret, for in this time period of the future, A chip called "The Human Ethical and Moral Epitome" chip or THEME chip was made to give the robots ethical and moral standards and even their own personality!</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">It means generative pre-trained transformer</span>
            <input type="text" v-model="text1" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text1 === 'GPT' || text1 == 'gpt'">
                <UTooltip text="W">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">W</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">SECURITY IMPROVED</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-50 h-full rounded-lg" src="../public/img/aisecurity.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">Enhanced security measures like security cameras paired with artificial intelligence to spot and signal emergency occurrences could shake up the security scene, and would pave the way for increased safety and emergencies able to be solved immediately! </span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">What's after a gigabyte? (Starts with T)</span>
            <input type="text" v-model="text2" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text2 === 'Terabyte' || text2 == 'terabyte'">
                <UTooltip text="O">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">O</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">AI AND I</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center bg-slate-400 justify-center">
            <img class="w-100 h-full rounded-lg hidden lg:block" src="../public/img/aiteamwork.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-3xl">In a world where we are afraid to embrace AI as it might slowly take over the world. However, there is great potential in the future where we would work together with Artificial Intelligence to make a better world around us and for the benefit of everyone</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">The A.I. from X (Starts with G)</span>
            <input type="text" v-model="text3" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text3 === 'Grok' || text3 == 'grok'">
                <UTooltip text="R">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">R</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-900 justify-start items-center min-h-55">
            <span class="text-white">Enter Passcode</span>
            <input type="text" v-model="passkey" class="rounded-lg w-20 font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="passkey === 'WOR' || passkey == 'wor'">
                <NuxtLink :to="`/mango/${2}`">
                    <div class="cursor-pointer w-content border-box pl-3 pr-3 shadow-md hover:shadow-xl text-shadow-md text-shadow-cyan-500 hover:text-shadow-lg transition-all ease shadow-cyan-500 min-h-15 bg-cyan-800 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">WOR</div>
                </NuxtLink>
            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        background-size: cover;
        background-position: center center;
        background-image: url(../public/img/aibg.gif)
    }
</style>