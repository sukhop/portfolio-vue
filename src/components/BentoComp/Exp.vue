
<script setup>
import ExpCard from './ExpCard.vue';
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
    <h2 class="text-2xl mb-3">Experience</h2>
    <div v-if="data" class="md:border-l border-slate-400 md:pl-7 md:py-3">
        <ExpCard v-for="(item, idx) in data.experiences" :key="idx" :des="data.experiences[idx].designation" :company="data.experiences[idx].companyName" :desc="data.experiences[idx].description" :time="data.experiences[idx].year"/>
    </div>
    <div v-else>
        LOADING
    </div>
</template>