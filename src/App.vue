<template>
  <div class="bg-[#111827] min-h-screen">
    <!-- Wrap components in Suspense to handle loading -->
     <Suspense>
      <template #default>
        <!-- Wrap all Components inside a single root element -->
         <div>
            <NavBar />
            <HeroSection />
            <!-- <ServicesSection /> -->
            <AboutSection />
            <ExperienceAndSkills />
            <LatestProjSection />
            <ContactSection />
            <!-- <TestimonialsSection /> -->
            <Footer />
            <BackToTop />
      </div>
    </template>
    <template #fallback>
      <div class="flex justify-center items-center min-h-screen">
          <loadingSpinner />
      </div>
    </template>
  </Suspense>
  </div>
</template>

<script setup>
 import { defineAsyncComponent } from 'vue';
//Import Components Asynchronously
const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const HeroSection = defineAsyncComponent(()=>import('@/components/HeroSection.vue'));
const ServicesSection = defineAsyncComponent(()=>import('@/components/ServicesSection.vue'));
const AboutSection = defineAsyncComponent(()=>import('@/components/AboutSection.vue'));
const TestimonialsSection = defineAsyncComponent(()=>import('@/components/TestimonialsSection.vue'));
const LatestProjSection = defineAsyncComponent(()=>import('@/components/LatestProjSection.vue'));
const ExperienceAndSkills = defineAsyncComponent(()=>import('@/components/ExperienceAndSkills.vue'));
const ContactSection = defineAsyncComponent(()=>import('@/components/ContactSection.vue'));
const Footer = defineAsyncComponent(()=>import('@/components/Footer.vue'));
const BackToTop = defineAsyncComponent(()=>import('@/components/BackToTop.vue'));
import loadingSpinner from './components/loadingSpinner.vue';
import { useHead } from '@vueuse/head';

useHead({
  title: 'Luca Neumann | Portfolio',
  meta: [
    { name: 'description', content: 'Official portfolio of Luca Neumann – HTL Anichstraße, Industrial Engineering & Business Informatics.' },
    { name: 'keywords', content: 'Luca Neumann, HTL Anichstraße, Portfolio, Junior Company, AlpenPro, Investment Banking' },
    { name: 'author', content: 'Luca Neumann' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1.0' },
    { charset: 'utf-8' },

    // Open Graph
    { property: 'og:title', content: 'Luca Neumann – Portfolio' },
    { property: 'og:description', content: 'Projects, news, and skills of Luca Neumann – student at HTL Anichstraße.' },
    { property: 'og:image', content: 'https://lucaneumann.com/icon.svg' },
    { property: 'og:url', content: 'https://lucaneumann.com' },
    { property: 'og:type', content: 'website' },

    // Twitter Card
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'twitter:title', content: 'Luca Neumann – Portfolio' },
    { name: 'twitter:description', content: 'Student, visionary, aspiring investment banker – discover my portfolio.' },
    { name: 'twitter:image', content: 'https://lucaneumann.com/icon.svg' },
  ],
  link: [
    { rel: 'icon', href: '/icon.svg' },
  ]
})

</script>
<style>

*{
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1;
}
</style>

