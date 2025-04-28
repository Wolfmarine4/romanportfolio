<script setup>
const projectItems = [
  { label: 'Science', to: '#science', icon: 'i-lucide-flask-conical' },
  { label: 'Art', to: '#art', icon: 'i-lucide-palette' },
  { label: 'Code', to: '#coding', icon: 'i-lucide-code-2' },
  { label: 'Music', to: '#music', icon: 'i-lucide-music' },
  { label: 'Photography', to: '#photography', icon: 'i-lucide-camera' }
]
</script>

<template>
  <!-- Projects Section -->
  <section id="projects" class="py-20 bg-white dark:bg-gray-900">
    <div class="container mx-auto px-4">
      
      <!-- Section Header -->
      <div class="text-center mb-16">
        <span class="inline-block text-sm font-medium uppercase tracking-wider text-slate-600 dark:text-slate-400 mb-2">
          Portfolio
        </span>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">
          My Projects
        </h2>
        <div class="w-16 h-1 bg-slate-700 dark:bg-slate-500 mx-auto"></div>
      </div>

      <!-- Project Navigation -->
      <div class="flex flex-wrap justify-center gap-4 mb-12">
        <UButton
          v-for="item in projectItems"
          :key="item.label"
          :to="item.to"
          :icon="item.icon"
          :label="item.label"
          variant="soft"
          color="gray"
          size="lg"
          class="font-medium"
        />
      </div>

      <!-- Project Sections -->
      <div class="space-y-24">

        <!-- Science Projects -->
        <section id="science" class="scroll-mt-24">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
            Science Projects
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <ProjectCard title="Water Quality Analysis" description="Conducted research on local water sources using chemical analysis techniques." />
            <ProjectCard title="Renewable Energy Experiment" description="Designed and built a small-scale solar energy collection system." />
          </div>
        </section>

        <!-- Art Projects -->
        <section id="art" class="scroll-mt-24">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
            Art Projects
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <ProjectCard title="Digital Landscapes" description="A series of digital paintings exploring futuristic landscapes and environments." />
            <ProjectCard title="Mixed Media Experiments" description="Combining traditional art techniques with digital tools for unique visual expressions." />
          </div>
        </section>

        <!-- Coding Projects -->
        <section id="coding" class="scroll-mt-24">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
            Coding Projects
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <ProjectCard title="Student Task Manager" description="A web application built to help students organize assignments and track progress." />
            <ProjectCard title="Python Game Development" description="Created a simple educational game using Python and Pygame libraries." />
          </div>
        </section>

        <!-- Music Projects -->
        <section id="music" class="scroll-mt-24">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
            Music Projects
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <ProjectCard title="Electronic Compositions" description="A collection of original electronic music pieces created with digital production tools." buttonLabel="Listen" />
            <ProjectCard title="School Jazz Ensemble" description="Performances and recordings with the school's award-winning jazz ensemble." buttonLabel="Listen" />
          </div>
        </section>

        <!-- Photography Projects -->
        <section id="photography" class="scroll-mt-24">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
            Photography Projects
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <ProjectCard title="Urban Nature Series" description="A photography series exploring natural elements within urban environments." buttonLabel="View Gallery" />
            <ProjectCard title="Student Portraits" description="A portrait series highlighting diverse students and their unique stories." buttonLabel="View Gallery" />
          </div>
        </section>

      </div>
    </div>
  </section>
</template>
