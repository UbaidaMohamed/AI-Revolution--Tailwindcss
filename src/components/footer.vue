<template>
    <footer class="footer">
        <div class="app-container">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-4 gap-12">
                <div class="space-y-4">
                    <div class="flex items-center">
                        <span class="gradient-text text-2xl font-bold">AI Revolution</span>
                    </div>
                    <p class="footer-description">
                        Pioneering AI Solutions for tomorrow's challenges. We empower businesses with cutting-edge artificial intelligence.
                    </p>
                    <div class="flex space-x-4 pt-2">
                        <a href="https://www.facebook.com" target="_blank" class="footer-social-link">
                            <AkFacebookFill class="w-6 h-6"/>
                        </a>
                        <a href="https://www.twitter.com" target="_blank" class="footer-social-link">
                            <AkTwitterFill class="w-6 h-6"/>
                        </a>
                        <a href="https://www.instagram.com" target="_blank" class="footer-social-link">
                            <AkInstagramFill class="w-6 h-6"/>
                        </a>
                        <a href="https://www.linkedin.com" target="_blank" class="footer-social-link">
                            <AkLinkedInFill class="w-6 h-6"/>
                        </a>
                    </div>
                </div>
                <div>
                    <h1 class="footer-title">Explore</h1>
                    <ul class="footer-link-list">
                        <li v-for="link in quickLinks">
                            <a :href="link.href" class="footer-link">
                                <AkCircleChevronRightFill class="mr-2"/>
                                {{ link.text }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h1 class="footer-title">Resources</h1>
                    <ul class="footer-link-list">
                        <li v-for="link in resources">
                            <a :href="link.href" class="footer-link">
                                <AkCircleChevronRightFill class="mr-2"/>
                                {{ link.text }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3 class="footer-title">Stay Updated</h3>
                    <p class="footer-newsletter-desc">
                        Subscribe to our newsletter for the latest AI insights and company news.
                    </p>
                    <form class="mt-4 flex flex-col sm:flex-row gap-2">
                        <input type="email" name="" id="" placeholder="Your Email" class="footer-newsletter-input">
                        <button class="footer-newsletter-btn">Subscribe</button>
                    </form>
                    <p class="footer-newsletter-privacy">We respect your privacy. Unsubscribe any time.</p>
                </div>
            </div>
            <div class="footer-bottom-bar">
                <p class="footer-bottom-text">
                    &copy; 2026 AI Revolution. All rights reserved.
                </p>
                <div class="footer-bottom-link-group">
                    <a href="#" class="footer-bottom-link">Terms of Service</a>
                    <a href="#" class="footer-bottom-link">Privacy Policy</a>
                    <a href="#" class="footer-bottom-link">Cookie Policy</a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>
import { AkFacebookFill, AkTwitterFill, AkInstagramFill, AkLinkedInFill, AkCircleChevronRightFill } from '@kalimahapps/vue-icons';

const quickLinks = [
  { text: "About Us", href: "#" },
  { text: "AI Technologies", href: "#types" },
  { text: "Case Studies", href: "#benefits" },
  { text: "Contact Us", href: "#contact" },
  { text: "Careers", href: "#" }
];

const resources = [
  { text: "Documentation", href: "#" },
  { text: "API Reference", href: "#" },
  { text: "Community Forum", href: "#" },
  { text: "Blog & News", href: "#" },
  { text: "Help Center", href: "#" }
];

</script>