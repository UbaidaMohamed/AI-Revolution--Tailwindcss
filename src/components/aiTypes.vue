<template>
    <section id="types" class="app-container py-16">
        <div class="text-center mb-12">
            <span class="section-subheader">AI Technologies</span>
            <h2 class="section-header">
                Different Types of <span class="gradient-text">Artificial Intelligence</span>
            </h2>
            <p class="section-description">
                Explore the diverce landscape of AI technologies that are shaping our future!
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <article v-for="type in aiTypes" class="ai-type-card">
                <img 
                :src="type.image" 
                :alt="type.title"
                class="ai-type-card-image">
                <div class="p-6">
                    <div class="flex items-center mb-3">
                        <div class="ai-type-card-icon">
                            <component :is="type.icon" class="h-8 w-8"/>
                        </div>
                        <h3 class="text-xl font-bold text-slate-300">
                            {{ type.title }}
                        </h3>
                    </div>
                    <p class="mt-2 text-gray-600 dark:text-slate-400"> {{ type.description }}</p>
                    <div class="mt-4 flex items-center gap-x-2">
                        <span v-for="tag in type.tags" :class="tagColors[tag.color] + ' ai-type-card-tag'"> {{ tag.text }}</span>
                    </div>
                </div>
            </article>
        </div>
    </section>
</template>

<script setup>
import { LightBulbIcon,
    EnvelopeIcon,
    ChatBubbleLeftRightIcon
} from '@heroicons/vue/24/outline'
    const aiTypes = [
        {
          title: "Machine Learning",
          description: "Systems that learn and improve from experience without being explicitly programmed.",
          image: "https://images.unsplash.com/photo-1555255707-c07966088b7b?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
          icon: LightBulbIcon,
          tags: [
            { text: "Predictive", color: "primary" },
            { text: "Adaptive", color: "secondary" }
          ],
        },
        {
          title: "Neural Networks",
          description: "Biologically inspired networks that simulate human brain functions for pattern recognition.",
          image: "https://images.unsplash.com/photo-1645839057098-5ea8761a6b09?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
          icon:
            EnvelopeIcon,
          tags: [
            { text: "Deep Learning", color: "primary" },
            { text: "Complex Data", color: "accent" }
          ],
        },
        {
          title: "Natural Language Processing",
          description: "Enabling machines to understand, interpret, and generate human language naturally.",
          image: "https://plus.unsplash.com/premium_photo-1733317429945-a3688f50430b?q=80&w=1915&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
          icon: ChatBubbleLeftRightIcon,
          tags: [
            { text: "Chatbots", color: "secondary" },
            { text: "Translation", color: "accent" }
          ],
        }
    ];

    const tagColors = {
    primary: "bg-primary/10 text-primary",
    secondary: "bg-secondary/10 text-secondary",
    accent: "bg-accent/10 text-accent",
    };
</script>