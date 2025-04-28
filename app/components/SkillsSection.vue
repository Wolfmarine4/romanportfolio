<template>
  <!-- Skills Section -->
  <section id="features" class="py-20 bg-gray-100 dark:bg-gray-800">
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <span class="inline-block text-sm font-medium uppercase tracking-wider text-slate-600 dark:text-slate-400 mb-2">
          Expertise
        </span>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">
          My Capabilities
        </h2>
        <div class="w-16 h-1 bg-slate-700 dark:bg-slate-500 mx-auto"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Technology & Development Card -->
        <div class="group">
          <div class="bg-white dark:bg-gray-900 p-8 border border-gray-200 dark:border-gray-700 rounded shadow-sm hover:shadow-md transition-shadow h-full">
            <div class="w-14 h-14 bg-slate-200 dark:bg-slate-700 rounded-sm flex items-center justify-center mb-6 group-hover:bg-slate-800 group-hover:text-white dark:group-hover:bg-slate-600 transition-colors">
              <Icon name="lucide:code-2" class="text-slate-700 dark:text-slate-300 text-2xl" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">
              Technology & Development
            </h3>
            <p class="text-gray-700 dark:text-gray-300 mb-6">
              Building digital solutions through code and design to solve problems and improve experiences. 
            </p>
            <div class="flex flex-wrap gap-2">
              <SkillTag label="Web Design" />
              <SkillTag label="Python" />
              <SkillTag label="UI/UX" />
            </div>
          </div>
        </div>

        <!-- Scientific Research Card -->
        <div class="group">
          <div class="bg-white dark:bg-gray-900 p-8 border border-gray-200 dark:border-gray-700 rounded shadow-sm hover:shadow-md transition-shadow h-full">
            <div class="w-14 h-14 bg-slate-200 dark:bg-slate-700 rounded-sm flex items-center justify-center mb-6 group-hover:bg-slate-800 group-hover:text-white dark:group-hover:bg-slate-600 transition-colors">
              <Icon name="lucide:flask-conical" class="text-slate-700 dark:text-slate-300 text-2xl" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">
              Scientific Research
            </h3>
            <p class="text-gray-700 dark:text-gray-300 mb-6">
              Exploring scientific principles through experiments and analysis to find effective solutions to real-world problems.
            </p>
            <div class="flex flex-wrap gap-2">
              <SkillTag label="Physics" />
              <SkillTag label="Chemistry" />
              <SkillTag label="Data Analysis" />
            </div>
          </div>
        </div>

        <!-- Creative Arts Card -->
        <div class="group">
          <div class="bg-white dark:bg-gray-900 p-8 border border-gray-200 dark:border-gray-700 rounded shadow-sm hover:shadow-md transition-shadow h-full">
            <div class="w-14 h-14 bg-slate-200 dark:bg-slate-700 rounded-sm flex items-center justify-center mb-6 group-hover:bg-slate-800 group-hover:text-white dark:group-hover:bg-slate-600 transition-colors">
              <Icon name="lucide:music" class="text-slate-700 dark:text-slate-300 text-2xl" />
            </div>
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">
              Creative Expression
            </h3>
            <p class="text-gray-700 dark:text-gray-300 mb-6">
              Creating music, photography, and digital art tnat communicates ideas and emotions.
            </p>
            <div class="flex flex-wrap gap-2">
              <SkillTag label="Music Production" />
              <SkillTag label="Photography" />
              <SkillTag label="Digital Design" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
