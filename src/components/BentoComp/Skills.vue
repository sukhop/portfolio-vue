<script setup>
import { onMounted, ref, computed } from 'vue';

const data = ref(null);

const path = (value) => `https://sukhop.vercel.app${value}`;

onMounted(async () => {
    try {
        const response = await fetch('https://raw.githubusercontent.com/RichestsoftSukhbir/portfolio-nextjs/main/src/config/text.json');

        if (response.ok) {
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
    <h2 class="mb-3 text-2xl">Skills</h2>
    <div v-if="data" v-for="(item, idx) in data.techCard.img" class="p-3 px-4 rounded-xl border bg-slate-800 text-slate-200 mb-3 grid grid-cols-[auto_1fr] gap-3 items-center">
        <div class="icon">
            <img :src=path(item) :alt="data.techCard.techText[idx]" class="h-10 w-10 object-contain">
        </div>
        <div class="name text-sm">
            {{ data.techCard.techText[idx] }}
        </div>
    </div>
</template>