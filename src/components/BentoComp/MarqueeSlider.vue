<script setup>
import { Vue3Marquee } from 'vue3-marquee';

const texts = ["Front-End Developer", "Web Designer", "Graphic Designer"];
</script>
<template>
    <Vue3Marquee>
        <div class="flex gap-5 items-center me-5" v-for="(item, index) in texts" :key="index">
            <h5 class="mb-0 text-3xl">{{ item }}</h5>
            <img alt="sparkel" width="25" height="25"  src="/images/sparkel.svg">
            <h2 class="text-5xl mb-0 primary-color">最強</h2>
            <span class="text font-bold text-center leading-tight">If You Don’t Take Risks,<br>You Can’t Create A Future.</span>
            <img alt="sparkel" width="25" height="25"  src="/images/sparkel.svg">
        </div>
    </Vue3Marquee>
</template>