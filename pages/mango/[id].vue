<script setup>
</script>

<template>
    <main class="w-screen h-screen flex justify-start items-center flex-col border-box p-20 gap-20 bg-black relative overflow-hidden">
        <div class="w-full flex flex-col items-center h-content z-[0]">
            <img src="../../public/img/test landing.gif" alt="" class="w-120 h-60">
            <span class="text-xl font-bold text-shadow-lg text-shadow-neutral-400">Take a glimpse into the Future</span>
        </div>
        <aside class="w-screen h-screen absolute opacity-10 t-0 l-0 bg-black">

        </aside>
        <div class="w-content items-center flex flex-col md:flex-row min-w-100 h-content gap-15">
            <NuxtLink to="/medicine" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700 bg-cyan-500 shadow-sm text-shadow-sm hover:shadow-xl hover:text-shadow-lg shadow-cyan-500 transition-all ease animated">
                <UIcon name="i-proicons-heart" size="50" class="bg-slate-700"></UIcon>
            </NuxtLink>
            <NuxtLink to="/ai" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700 bg-cyan-500 shadow-sm text-shadow-sm hover:shadow-xl hover:text-shadow-lg shadow-cyan-500 transition-all ease animated">
                <UIcon name="i-proicons-terminal" size="50" class="bg-slate-700"></UIcon>
            </NuxtLink>
            <div v-if="useRoute().params.id < 2" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700">
                <UIcon name="i-proicons-leaf-three" size="50" class="bg-slate-700"></UIcon>
                <UIcon name="i-proicons-lock" size="50" class="bg-slate-700"></UIcon>
            </div>
            <NuxtLink v-else to="/nature" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700 bg-cyan-500 shadow-sm text-shadow-sm hover:shadow-xl hover:text-shadow-lg shadow-cyan-500 transition-all ease animated">
                <UIcon name="i-proicons-leaf-three" size="50" class="bg-slate-700"></UIcon>
            </NuxtLink>
            <div v-if="useRoute().params.id < 3" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700">
                <UIcon name="i-proicons-game" size="50" class="bg-slate-700"></UIcon>
                <UIcon name="i-proicons-lock" size="50" class="bg-slate-700"></UIcon>
            </div>
            <NuxtLink v-else to="/gaming" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700 bg-cyan-500 shadow-sm text-shadow-sm hover:shadow-xl hover:text-shadow-lg shadow-cyan-500 transition-all ease animated">
                <UIcon name="i-proicons-game" size="50" class="bg-slate-700"></UIcon>
            </NuxtLink>
            <div v-if="useRoute().params.id < 4" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700">
                <UIcon name="i-proicons-drop" size="50" class="bg-slate-700"></UIcon>
                <UIcon name="i-proicons-lock" size="50" class="bg-slate-700"></UIcon>
            </div>
            <NuxtLink v-else to="/ocean" class="flex flex-col items-center justify-center w-20 h-20 rounded-full border-solid border-2 border-box p-2 border-slate-700 bg-cyan-500 shadow-sm text-shadow-sm hover:shadow-xl hover:text-shadow-lg shadow-cyan-500 transition-all ease animated">
                <UIcon name="i-proicons-drop" size="50" class="bg-slate-700"></UIcon>
            </NuxtLink>
        </div>
        <NuxtLink v-if="useRoute().params.id == 5" to="/earth" class="flex flex-col items-center justify-center w-30 h-30 rounded-full border-solid border-2 border-box p-2 border-slate-700 bg-cyan-500 shadow-sm text-shadow-sm hover:shadow-xl hover:text-shadow-lg shadow-cyan-500 transition-all ease">
            <UIcon name="i-proicons-globe" size="120" class="bg-slate-700"></UIcon>
        </NuxtLink>
    </main>
</template>

<style>
</style>