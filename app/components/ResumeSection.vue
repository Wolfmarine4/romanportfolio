<template>
    <section id="resume" class="py-20 bg-gray-100 dark:bg-gray-800">
      <div class="container mx-auto px-4">
        <div class="max-w-4xl mx-auto">
          <!-- Section Header -->
          <div class="text-center mb-16">
            <span class="inline-block text-sm font-medium uppercase tracking-wider text-slate-600 dark:text-slate-400 mb-2">
              Experience
            </span>
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">
              My Resume
            </h2>
            <div class="w-16 h-1 bg-slate-700 dark:bg-slate-500 mx-auto"></div>
          </div>
  
          <!-- Resume Card -->
          <div class="bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-8 rounded shadow-sm space-y-16">
            
            <!-- Objective Section -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Objective
              </h3>
              <p class="text-gray-700 dark:text-gray-300">
                Aspiring data scientist with a strong foundation in coding, database organization, and data analysis. Passionate about applying technology to real-world scientific problems. Excels in structured learning environments and self-paced virtual study. Completed dual coursework in web design and art appreciation at Lone Star College while maintaining a 4.0 unweighted GPA.
              </p>
            </section>
  
            <!-- Education Section - FIXED with bulleted points -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Education
              </h3>
              <div class="relative pl-8 border-l border-gray-200 dark:border-gray-700 space-y-8">
                <div class="relative">
                  <div class="absolute -left-2 top-1 w-4 h-4 rounded-full bg-slate-700 dark:bg-slate-500"></div>
                  <h4 class="text-lg font-semibold text-gray-900 dark:text-white">
                    iSchool Virtual Academy
                  </h4>
                  <p class="text-sm text-slate-600 dark:text-slate-400 mb-1">Expected Graduation: 2027</p>
                  <ul class="list-disc pl-5 text-gray-700 dark:text-gray-300 mt-2">
                    <li>Weighted GPA: 4.1</li>
                    <li>Accelerated Mathematics Program</li>
                    <li>Computer Science Pathway</li>
                  </ul>
                </div>
  
                <div class="relative">
                  <div class="absolute -left-2 top-1 w-4 h-4 rounded-full bg-slate-700 dark:bg-slate-500"></div>
                  <h4 class="text-lg font-semibold text-gray-900 dark:text-white">
                    Lone Star College
                  </h4>
                  <p class="text-sm text-slate-600 dark:text-slate-400 mb-1">2023 – 2024</p>
                  <ul class="list-disc pl-5 text-gray-700 dark:text-gray-300 mt-2">
                    <li>Dual coursework: Web Design and Art Appreciation</li>
                    <li>4.0 GPA</li>
                    <li>Completed college-level coursework while in high school</li>
                  </ul>
                </div>
              </div>
            </section>
  
            <!-- Extracurricular Activities Section -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Extracurricular Activities
              </h3>
              <ul class="list-disc list-inside text-gray-700 dark:text-gray-300 space-y-2">
                <li>Self-directed learning in data visualization and database tools</li>
                <li>Brazilian Jiu Jitsu</li>
                <li>Tae Kwon Do</li>
              </ul>
            </section>
  
            <!-- Volunteer Experience Section -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Volunteer Work
              </h3>
              <ul class="list-disc list-inside text-gray-700 dark:text-gray-300 space-y-2">
                <li>Academy 4 Volunteer (2019) - Assisted with packing food for homeless shelters</li>
              </ul>
            </section>
  
            <!-- Achievements Section -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Achievements
              </h3>
              <ul class="list-disc list-inside text-gray-700 dark:text-gray-300 space-y-2">
                <li>A Honor Roll Student - 6 consecutive years</li>
                <li>TSI2 Completion Certificate</li>
                <li>Udemy Adobe Mastery Certificate</li>
              </ul>
            </section>
  
            <!-- Skills Section -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Skills
              </h3>
              <ul class="list-disc list-inside text-gray-700 dark:text-gray-300 space-y-2">
                <li>Coding (Nuxt.js, Vue 3, HTML, CSS)</li>
                <li>Data Science & Analytics (collecting, organizing, and analyzing data)</li>
                <li>Database Organization (Notion.so)</li>
              </ul>
            </section>
  
            <!-- References Section -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                References
              </h3>
              <div class="text-gray-700 dark:text-gray-300 space-y-4">
                <div>
                  <p class="font-medium">Amber Kennedy</p>
                  <p class="text-sm">ankennedy@responsiveedtx.com | 940-799-9870</p>
                </div>
                <div>
                  <p class="font-medium">Ryan Roberts</p>
                  <p class="text-sm">jaroberts@responsiveedtx.com</p>
                </div>
              </div>
            </section>
  
            <!-- Download Resume Button -->
            <div class="text-center">
              <UButton
                label="Download Full Resume (PDF)"
                icon="i-lucide-download"
                to="/Roman-Ross-Resume.pdf"
                color="gray"
                class="bg-slate-800 hover:bg-slate-700 dark:bg-slate-700 dark:hover:bg-slate-600 text-white font-medium"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
