<template>
  <div class="container mx-auto px-4 relative z-10 py-12 md:py-24">
    <div class="flex flex-col items-center justify-between gap-8 md:gap-16">
      <div class="md:w-5/12 order-first md:order-none flex justify-center">
        <div class="relative mx-auto w-64 h-64 md:w-80 md:h-80">
          <div class="absolute inset-0 border-2 border-slate-400 dark:border-slate-600 rounded-sm transform rotate-6"></div>
          <div class="absolute inset-0 border-2 border-slate-700 dark:border-slate-400 rounded-sm transform -rotate-3"></div>
          <div class="relative overflow-hidden rounded-sm border-4 border-white dark:border-gray-800 shadow-xl h-full">
            <div style="width: 100%; height: 100%; background-image: url('/Roman-headshot.png'); background-size: cover; background-position: center;"></div>
          </div>
        </div>
      </div>
      <div class="md:w-6/12 text-center">
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 dark:text-white mb-4 leading-tight">
          Roman Ross
        </h1>
        <div class="w-20 h-1 bg-slate-700 dark:bg-slate-400 mb-6 mx-auto"></div>
        <p class="text-lg md:text-xl text-gray-700 dark:text-gray-300 mb-8 max-w-lg mx-auto">
          Bringing together technology, science, and creativity to develop new ideas and solutions.
        </p>

        <div class="flex flex-wrap gap-4 justify-center">
          <UButton
            label="View Projects"
            to="#projects"
            size="lg"
            color="gray"
            class="bg-slate-800 hover:bg-slate-700 dark:bg-slate-700 dark:hover:bg-slate-600 text-white font-medium"
          />
          <UButton
            label="Contact"
            to="#contact"
            size="lg"
            variant="outline"
            color="gray"
            class="border-slate-800 text-slate-800 hover:bg-slate-100 dark:border-slate-400 dark:text-slate-200 dark:hover:bg-slate-800/50 font-medium"
          />
        </div>
      </div>
    </div>
  </div>
</template>
