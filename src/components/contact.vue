<template>
    <section id="contact" class="app-container py-16">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div>
                <span class="section-subheader">Get in Touch</span>
                <h2 class="section-header">
                    Ready to <span class="gradient-text">Transform</span> Your Business with AI
                </h2>
                <p class="section-description">
                    Our team of AI experts is ready to help you implement cutting-edge solutions tailored to your specific needs. Contact
                </p>
                <div class="mt-8 space-y-4">
                    <div v-for="detail in contactDetails" class="contact-info-group">
                        <component :is="detail.icon" class="form-icon"/>
                        <div>
                            <h3 class="contact-title">{{ detail.title }}</h3>
                            <p class="contact-text">{{ detail.text }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="bg-white rounded-xl shadow-lg p-6 lg:p-8 dark:bg-slate-800">
                <form>
                    <div class="space-y-6">
                        <div>
                            <label class="form-input-label">Full Name</label>
                            <input type="text" class="form-input">
                        </div>
                        <div>
                            <label class="form-input-label">Email Address</label>
                            <input type="email" class="form-input">
                        </div>
                        <div>
                            <label class="form-input-label">Subject</label>
                            <input type="text" class="form-input">
                        </div>
                        <div>
                            <label class="form-input-label">Message</label>
                            <textarea class="form-input" rows="4"/>
                        </div>
                    </div>
                    <button class="btn-primary w-full mt-6">Send Message</button>
                </form>
            </div>
        </div>
    </section>
</template>

<script setup>
import {
  PhoneIcon,
  EnvelopeIcon,
  MapPinIcon,
} from "@heroicons/vue/24/outline";

const contactDetails = [
  {
    title: "Phone",
    text: "+1 (555) 123-4567",
    icon: PhoneIcon,
  },
  {
    title: "Email",
    text: "contact@airevolution.com",
    icon: EnvelopeIcon,
  },
  {
    title: "Office",
    text: "123 AI Boulevard, Tech City, TC 10001",
    icon: MapPinIcon,
  },
];
</script>