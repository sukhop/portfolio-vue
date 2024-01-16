<script setup>
const year = new Date().getFullYear();
</script>

<template>
    <footer class="w-full">
        <div class="px-3 mb-3">
            <nav class="footer stripes flex justify-end items-center border border-black bg-white">
                <div class="inline-flex py-2 px-6 border-l border-black items-center bg-yellow-300 font-bold logo-text">
                    <p class="text-sm">&copy;{{ year }} <a href="https://sukhop.vercel.app/" target="_blank">SukhFX</a>.</p>
                </div>
            </nav>
        </div>
    </footer>
</template>