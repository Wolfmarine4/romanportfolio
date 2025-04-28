<script setup>
import HeroSection from '~/components/HeroSection.vue'
import AboutMe from '~/components/AboutMe.vue'
import ResumeSection from '~/components/ResumeSection.vue'
import ContactSection from '~/components/ContactSection.vue'
import SkillsSection from '~/components/SkillsSection.vue'

useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' },
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Bitter:wght@500;700&display=swap' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = "Roman Ross | Portfolio"
const description = "Student. Creator. Innovator."
useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/social-card.png',
  twitterImage: '/social-card.png',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <UApp class="sophisticated-portfolio">
    <!-- Main Content Sections -->
    <HeroSection />
    <AboutMe />
    <SkillsSection />
    <ResumeSection />
    <ContactSection />
  </UApp>
</template>

<style scoped>
.sophisticated-portfolio {
  font-family: 'Poppins', sans-serif;
}
.sophisticated-portfolio h1,
.sophisticated-portfolio h2,
.sophisticated-portfolio h3 {
  font-family: 'Bitter', serif;
}
</style>
