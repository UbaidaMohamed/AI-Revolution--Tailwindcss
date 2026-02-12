<template>
    <section id="benefits" class="app-container py-16 bg-gradient-to-br from-dark to-gray-900 dark:bg-gradient-to-l from-sky-300/30 to-pink-300/20 rounded-3xl text-white">
        <div class="text-center mb-12">
            <span class="section-subheader">AI Benefits</span>
            <h2 class="section-header">
                How AI is <span class="gradient-text">Transforming Our World</span>
            </h2>
            <p class="section-description text-gray-300 dark:text-slate-400">
                Discover the positive impact of AI across various sectors and industries
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div class="benefit-card" v-for="benefit in benefits">
                <div :class="colorClasses[benefit.color] + ' benefit-card-icon'">
                    <component :is="benefit.icon" class="h-8 w-8"/>
                </div>
                <h3 class="text-xl font-bold text-white dark:text-slate-300">{{ benefit.title }}</h3>
                <p class="mt-2 text-gray-300 dark:text-slate-400">{{ benefit.description }}</p>
            </div>
        </div>
    </section>
</template>

<script setup>
import { 
    HeartIcon, 
    CurrencyDollarIcon, 
    ShieldCheckIcon, 
    BoltIcon, 
    CloudIcon, 
    BookOpenIcon 
} from '@heroicons/vue/24/outline'

const benefits = [
    {
      title: "Healthcare Advancements",
      description:
        "AI enables faster diagnosis, personalized treatment plans, and drug discovery, saving countless lives.",
      icon: HeartIcon,
      color: "primary",
    },
    {
      title: "Economic Growth",
      description:
        "AI-driven automation and insights contribute to increased productivity and economic expansion.",
      icon: CurrencyDollarIcon,
      color: "secondary",
    },
    {
      title: "Enhanced Security",
      description:
        "AI-powered systems detect and prevent cyber threats and fraud more effectively than traditional methods.",
      icon: ShieldCheckIcon,
      color: "accent",
    },
    {
      title: "Energy Efficiency",
      description:
        "AI optimizes energy consumption in industries and homes, reducing waste and environmental impact.",
      icon: BoltIcon,
      color: "primary",
    },
    {
      title: "Climate Solutions",
      description:
        "AI models help predict climate patterns and develop strategies to combat climate change.",
      icon: CloudIcon,
      color: "secondary",
    },
    {
      title: "Education Access",
      description:
        "AI-powered platforms provide personalized learning experiences to students worldwide.",
      icon: BookOpenIcon,
      color: "accent",
    },
  ];

  const colorClasses = {
    primary: "bg-primary/10 text-primary",
    secondary: "bg-secondary/10 text-secondary",
    accent: "bg-accent/10 text-accent",
  };
</script>