<script setup>
    const text1 = ref('')
    const text2 = ref('')
    const text3 = ref('')
    const passkey = ref('')
</script>

<template>
    <main class="w-screen h-screen flex justify-start items-center flex-col border-box gap-5 pt-10 pb-10 overflow-y-auto">
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content m-5 text-center max-w-300 bg-slate-300 justify-center">
            <span class="text-4xl text-black font-bold">MEDICINE</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">ADVANCED HEALTHCARE TECHNOLOGY</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-50 h-full rounded-lg" src="../public/img/medtech.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">Experience the great advancements of technology as it gets applied to the field of medicine! A world where technology paired with the usage of artificial intelligence gets to take the stage on curing various sicknesses! </span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">Ailment that indicate you have a sickness? (Starts with S)</span>
            <input type="text" v-model="text1" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text1 === 'Symptom' || text1 == 'symptom'">
                <UTooltip text="N">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">N</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">THE MEDICAL BLASTER</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <img class="w-50 h-full rounded-lg" src="../public/img/medgun.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">A futuristic invention that is able to cure sicknesses with one trigger. It may revolutionize the field of medicine with the concept of instant healing and recovery, granting the ability to save lives (at maybe an expensive cost) </span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">Another word for a first-aid kit (Starts with M)</span>
            <input type="text" v-model="text2" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text2 === 'Medkit' || text2 == 'medkit'">
                <UTooltip text="E">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">E</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-400 justify-center">
            <span class="text-4xl text-black font-bold">REJUVENATING MUSIC</span>
        </div>
        <div class="flex gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center bg-slate-400 justify-center">
            <img class="w-100 h-full rounded-lg hidden lg:block" src="../public/img/medsong.jpg" />
            <span class="text-md text-black font-bold max-w-100 text-justify text-xl">An actual recent study and experiment was conducted on dead coral reefs that playing the sounds of healthy coral reefs nearby, would eventually heal the dead reefs. From this, studies can continue until they can discover how to turn MUSIC into a medical tool to heal and lift people's spirits at the same time! It may revolutionize holistic care as a whole.</span>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-700 justify-start items-center min-h-52">
            <span class="text-white">Another word for a Doctor in a medical setting (Starts with P)</span>
            <input type="text" v-model="text3" class="rounded-lg w-full font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="text3 === 'Physician' || text3 == 'physician'">
                <UTooltip text="O">
                    <div class="cursor-pointer w-15 min-h-15 bg-slate-900 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">O</div>
                </UTooltip>
            </div>
        </div>
        <div class="flex flex-col gap-3 border-box p-5 rounded-lg shadow-lg shadow-cyan-500/50 min-w-sm w-content mr-10 ml-10 text-center max-w-300 bg-slate-900 justify-start items-center min-h-55">
            <span class="text-white">Enter Passcode</span>
            <input type="text" v-model="passkey" class="rounded-lg w-20 font-white bg-slate-800 border-box p-5 text-xl"/>
            <div v-show="passkey === 'NEO' || passkey == 'neo'">
                <NuxtLink :to="`/mango/${1}`">
                    <div class="cursor-pointer w-content border-box pl-3 pr-3 shadow-md hover:shadow-xl text-shadow-md text-shadow-cyan-500 hover:text-shadow-lg transition-all ease shadow-cyan-500 min-h-15 bg-cyan-800 text-white text-5xl rounded-xl text-center flex items-center justify-center" style="font-family: 'Wingdings'">NEO</div>
                </NuxtLink>
            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        background-size: cover;
        background-position: center center;
        background-image: url(../public/img/medbg.gif)
    }
</style>