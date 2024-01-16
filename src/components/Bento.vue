<script setup>
import IntroSec from './BentoComp/Intro.vue';
import MarqueeSlider from './BentoComp/MarqueeSlider.vue';
import About from './BentoComp/About.vue';
import Exp from './BentoComp/Exp.vue';
import Social from './BentoComp/Social.vue';
import Skills from './BentoComp/Skills.vue';
</script>

<style>
@tailwind components;

@layer components {
    .bento-box {
        @apply bg-slate-900 bg-opacity-10 border border-slate-300 backdrop-blur-sm px-3 py-5 rounded-2xl;
    }
}

.intro {
    display: flex;
    align-items: flex-end;
}
</style>

<template>
    <div class="bento-grid grid md:grid-cols-4 md:grid-rows-5 md:h-full p-3 gap-3">
        <div class="bento-box intro md:row-span-3 md:col-span-1 grid-pat">
            <IntroSec/>
        </div>
        <div class="bento-box about md:row-span-2 md:col-span-2 overflow-y-auto no-scrollbar">
            <About/>
        </div>
        <div class="bento-box skills md:row-span-2 md:col-span-1 grid-pat overflow-y-auto no-scrollbar">
            <Skills/>
        </div>
        <div class="marquee md:row-span-1 md:col-span-2 flex items-center overflow-hidden">
            <MarqueeSlider/>
        </div>
        <div class="social md:row-span-3 md:col-span-1">
            <Social/>
        </div>
        <div class="bento-box contact md:row-span-2 md:col-span-2 grid-pat"></div>
        <div class="bento-box exp md:row-span-2 md:col-span-1 grid-pat no-scrollbar md:overflow-y-auto">
            <Exp/>
        </div>
    </div>
</template>