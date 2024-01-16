<script setup>
import Bento from './components/Bento.vue';
import Navbar from './components/Navbar.vue';
import Footbar from './components/Footbar.vue';
</script>

<template>
  <Navbar/>
  <main class="px-3">
    <div class="border-x border-black h-[calc(100dvh-120px)] overflow-y-auto no-scrollbar">
      <Bento/>
    </div>
  </main>
  <Footbar/>
</template>