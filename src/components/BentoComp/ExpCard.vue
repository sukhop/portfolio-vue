<script setup>
const props = defineProps(['des', 'company', 'desc', 'time']);
</script>

<template>
    <div class="last:border-b-0 border-b border-slate-400 pb-7 mb-7 last:mb-0 last:pb-0 relative after:content-[unset] md:after:content-[''] after:w-3 after:h-3 after:bg-slate-400 after:absolute after:top-2 after:-left-[34px] after:rounded-xl">
        <h3 class="text-xl">{{ des }}</h3>
        <p class="mb-2">{{ company }}</p>
        <p class="text-sm text-slate-500 mb-2">{{ time }}</p>
        <p v-html="desc" class="max-w-96"></p>
    </div>
</template>