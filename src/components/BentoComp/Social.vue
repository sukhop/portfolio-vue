<script setup>

const socialEl = [
    { icon: "fa-brands fa-facebook-f", link: 'https://www.facebook.com/sukhhacking.yt.5', name: "Facebook" },
    { icon: "fa-brands fa-x-twitter", link: 'https://twitter.com/sukh_fx', name: "XTwitter" },
    { icon: "fa-brands fa-instagram", link: 'https://www.instagram.com/sukhfx/', name: "Instagram" },
    { icon: "fa-brands fa-linkedin-in", link: 'https://www.linkedin.com/in/sukhfx/', name: "LinkedinIn" },
    { icon: "fa-solid fa-at", link: 'mailto:sukhbircing@gmail.com', name: "Envelope" },
    { icon: "fa-brands fa-github", link: 'https://github.com/sukhop', name: "Github" },
    { icon: "fa-brands fa-whatsapp", link: 'https://wa.me/+918168387411', name: "Whatsapp" },
    { icon: "fa-brands fa-codepen", link: 'https://codepen.io/sukhbir_singh', name: "Codepen" },
    { icon: "fa-brands fa-discord", link: 'https://discord.com/users/457830738923094028', name: "Discord" }
];

</script>

<template>
    <div class="grid grid-rows-3 grid-cols-3 h-full gap-3">
        <a :href="item.link" v-for="(item, idx) in socialEl" :key="idx" class="bento-box flex justify-center items-center text-xl md:text-2xl lg:text-4xl hover:text-purple-600 transition ease-in" target="_blank">
            <i :class="item.icon"></i>
        </a>
    </div>
</template>