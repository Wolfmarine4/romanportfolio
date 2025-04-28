<script setup>
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = "Roman Ross - High School Portfolio"
const description = "Welcome to Roman Ross's high school portfolio showcasing projects, achievements, and skills developed throughout my academic journey."
useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/social-card.png',
  twitterImage: '/social-card.png',
  twitterCard: 'summary_large_image'
})

// Project showcase items
const projectItems = [
  { label: 'Science Fair', to: '#science-fair', icon: 'i-lucide-flask' },
  { label: 'Art Gallery', to: '#art-gallery', icon: 'i-lucide-paintbrush' },
  { label: 'Coding Projects', to: '#coding', icon: 'i-lucide-code' },
  { label: 'Volunteer Work', to: '#volunteer', icon: 'i-lucide-heart-handshake' },
  { label: 'Sports Achievements', to: '#sports', icon: 'i-lucide-trophy' }
]
</script>

<template>
  <UApp>
    <UHeader :ui="{ wrapper: 'justify-between' }">
      <template #left>
        <UColorModeButton />
        <!-- Social Media Icons -->
        <div class="flex items-center space-x-2">
          <UButton
            to="https://github.com/romanross"
            target="_blank"
            icon="i-simple-icons-github"
            aria-label="GitHub"
            color="neutral"
            variant="ghost"
          />
          <UButton
            to="https://instagram.com/romanross"
            target="_blank"
            icon="i-simple-icons-instagram"
            aria-label="Instagram"
            color="neutral"
            variant="ghost"
          />
          <UButton
            to="https://linkedin.com/in/romanross"
            target="_blank"
            icon="i-simple-icons-linkedin"
            aria-label="LinkedIn"
            color="neutral"
            variant="ghost"
          />
        </div>
      </template>
      
      <!-- Navigation Links - Both Desktop and Mobile -->
      <div class="hidden md:flex items-center space-x-6">
        <a href="#" class="hover:text-gray-300">Home</a>
        <a href="#about" class="hover:text-gray-300">About Me</a>
        <a href="#resume" class="hover:text-gray-300">Academic Resume</a>
        <a href="#contact" class="hover:text-gray-300">Contact</a>
      </div>
      
      <template #right>
        <!-- Mobile Menu Configuration -->
        <UNavigationLinks
          class="md:hidden"
          :links="[
            { label: 'Home', to: '#' },
            { label: 'About Me', to: '#about' },
            { label: 'Academic Resume', to: '#resume' },
            { label: 'Contact', to: '#contact' },
            { 
              label: 'Project Showcase', 
              children: projectItems 
            }
          ]"
        />
      </template>
    </UHeader>
    
    <UMain>
      <NuxtPage />
    </UMain>
    
    <USeparator />
    
    <UFooter>
      <template #left>
        <p class="text-sm text-muted">
          Roman Ross © {{ new Date().getFullYear() }} | Dallas, TX
        </p>
      </template>
      <template #right>
        <!-- Social Media Icons in Footer -->
        <div class="flex items-center space-x-2">
          <UButton
            to="https://github.com/romanross"
            target="_blank"
            icon="i-simple-icons-github"
            aria-label="GitHub"
            color="neutral"
            variant="ghost"
          />
          <UButton
            to="https://instagram.com/romanross"
            target="_blank"
            icon="i-simple-icons-instagram"
            aria-label="Instagram"
            color="neutral"
            variant="ghost"
          />
          <UButton
            to="https://linkedin.com/in/romanross"
            target="_blank"
            icon="i-simple-icons-linkedin"
            aria-label="LinkedIn"
            color="neutral"
            variant="ghost"
          />
        </div>
      </template>
    </UFooter>
  </UApp>
</template>