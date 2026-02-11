<template>
    <nav className="bg-white/80 backdrop-blur-md shadow-sm fixed w-full z-50">
        <div className="app-container flex justify-between items-center h-16">
            <span className="gradient-text text-2xl font-bold">
                AI Revolution
            </span>
            <div class="hidden md:flex items-center space-x-8">
                <a v-for="link in links" :key="link.name" className="nav-item" :href="link.href">
                    {{  link.name }}
                </a>
                <a href="#" className="nav-btn">Get Started</a>
            </div>
            <button @click="mobileMenuOpen = !mobileMenuOpen" className="md:hidden p-4 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none -space-y-4 h-16 font-extrabold">
                <MagnifyingGlassCircleIcon />
            </button>
        </div>
        <div v-if="mobileMenuOpen" className="md:hidden pb-3 bg-white shadow-lg rounded-b-lg px-2 pt-2 space-y-1">
            <a v-for="link in links" :key="link.name" className="mobile-nav-item" :href="link.href">
                    {{  link.name }}
            </a>
            <a href="#" className="mobile-nav-btn">Get Started</a>
        </div>
    </nav>
</template>

<script setup>
    import { MagnifyingGlassCircleIcon } from '@heroicons/vue/24/outline';
    import { ref } from 'vue';

    const mobileMenuOpen = ref(false);
    const links = [
        {name: "Home", href: "#home"},
        {name: "AI Types", href: "#types"},
        {name: "Benefits", href: "#benefits"},
        {name: "Contact", href: "#contact"}
    ]
</script>