<template>
    <section id="home" className="app-container pt-24 pb-12 overflow-hidden sm:overflow-visible">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div className="space-y-6">
                <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight">
                    <span class="gradient-text">Artificial Intelligence</span>
                    for a Smarter Future
                </h1>
                <p class="text-lg text-gray-600 max w-lg">
                    Discover how AI is transforming industries and improving lives worldwide. Our cutting-edge solutions harness the power of machine learning to solve complex problems.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 pt-4">
                    <a href="#" className="btn-primary">Explore AI Solutions</a>
                    <a href="#" className="btn-outline">Learn More</a>
                </div>
                <div class="pt-4 flex items-center space-x-4">
                    <div className="flex -space-x-2">
                        <img v-for="img in imgs" :src="img" alt="user" className="avatar">
                    </div>
                    <p className="text-sm font-medium text-gray-600">
                        Trusted by <span className="text-primary font-bold">10,000+</span> people worldwide
                    </p>
                </div>
            </div>
            <div className="w0full h-80 md:h-[600px]">
                <img className="w-full h-full object-cover rounded-2xl" src="../imgs/4.avif" alt="hero section">
                <div class="absolute w-32 h-32 rounded-full bg-secondary/20 -bottom-6 -left-6 blur-xl"></div>
                <div class="absolute w-32 h-32 rounded-full bg-accent/20 -top-3 -right-6 blur-xl"></div>
            </div>
        </div>
    </section>
</template>

<script setup>
    const imgs = ['../imgs/1.avif', '../imgs/2.avif', '../imgs/3.avif']
</script>