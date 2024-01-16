<script setup>
import { onMounted, ref } from 'vue';

const data = ref(null);

onMounted(async () => {
    try {
        const response = await fetch('https://raw.githubusercontent.com/RichestsoftSukhbir/portfolio-nextjs/main/src/config/text.json');

        if(response.ok) {
            data.value = await response.json();
        } else {
            console.error('Error fetching data:', response.statusText);
        }
    } catch (error) {
        console.error('Error fetching data:', error);
    }
});

</script>
<template>
    <h2 class="mb-3 text-2xl">About Me</h2>
    <p v-if="data" v-for="(text, index) in data.aboutText" class="mb-3 last:mb-0" v-html="text" :key="index"></p>
    <p v-else>LOADING</p>
</template>