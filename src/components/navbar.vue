<template>
    <nav class="bg-white/80 dark:bg-slate-950 backdrop-blur-md shadow-sm fixed w-full z-50">
        <div class="app-container flex justify-between items-center h-16">
            <span class="gradient-text text-2xl font-bold">
                AI Revolution
            </span>
            <div class="hidden md:flex items-center space-x-5">
                <a v-for="link in links" :key="link.name" class="nav-item" :href="link.href">
                    {{  link.name }}
                </a>
                <a href="#" class="nav-btn">Get Started</a>
                <button class="rounded-md cursor-pointer px-1" @click="toggle">
                    <PhFillMoonStars v-if="!isDark" class="mt-1 h-8 w-8"/>
                    <FlFilledWeatherSunny v-else class="mt-1 h-8 w-8 text-yellow-500 pb-1"/>
                </button>
            </div>
            <div class="md:hidden">
                <button @click="mobileMenuOpen = !mobileMenuOpen" class="dark:bg-slate-700 p-2 rounded-md bg-gray-100  foucs:outline-none">
                    <IoMenu class="h-8 w-8 text-gray-400 dark:text-gray-200 active:text-gray-500 dark:bg-slate-800"/>
                </button>
                <button class="bg-slate-300 rounded-md px-2" @click="toggle">
                    <PhFillMoonStars class="mt-1 h-8 w-8"/>
                </button>
            </div>
        </div>
        <div v-if="mobileMenuOpen" class="md:hidden dark:bg-slate-800 pb-3 bg-white shadow-lg rounded-b-lg px-2 pt-2 space-y-1">
            <div class="flex-col">
            <a v-for="link in links" :key="link.name" class="mobile-nav-item dark:text-gray-100  border-b border-gray-700" :href="link.href">
                    {{  link.name }}
            </a>
            </div>
            <a href="#" class="mobile-nav-btn">Get Started</a>
        </div>
    </nav>
</template>

<script setup>
    import { ref, onMounted } from 'vue';
    import { IoMenu, PhFillMoonStars, FlFilledWeatherSunny } from '@kalimahapps/vue-icons';
    
    onMounted(() => {
        isDark.value = localStorage.getItem('theme') === 'dark';
        if (isDark.value) {
            document.documentElement.classList.add('dark');
        }
    })

    const toggle = () => {
        isDark.value = !isDark.value;
        document.documentElement.classList.toggle('dark');
        localStorage.setItem('theme', isDark.value ? 'dark' : 'light');
    }

    const mobileMenuOpen = ref(false);
    const isDark = ref(false);

    const links = [
        {name: "Home", href: "#home"},
        {name: "AI Types", href: "#types"},
        {name: "Benefits", href: "#benefits"},
        {name: "Contact", href: "#contact"}
    ]
</script>