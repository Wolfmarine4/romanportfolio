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
  
            <!-- Education Section - FIXED with custom formatting -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Education
              </h3>
              <div class="relative pl-8 border-l border-gray-200 dark:border-gray-700 space-y-12">
                <div class="relative">
                  <h4 class="text-lg font-semibold text-gray-900 dark:text-white">
                    iSchool Virtual Academy
                  </h4>
                  <p class="text-sm text-slate-600 dark:text-slate-400 mb-3">Expected Graduation: 2027</p>
                  <div class="pl-5 mt-3">
                    <div class="text-gray-700 dark:text-gray-300 mb-1">• Weighted GPA: 4.1</div>
                    <div class="text-gray-700 dark:text-gray-300 mb-1">• Accelerated Mathematics Program</div>
                    <div class="text-gray-700 dark:text-gray-300">• Computer Science Pathway</div>
                  </div>
                </div>
  
                <div class="relative">
                  <h4 class="text-lg font-semibold text-gray-900 dark:text-white">
                    Lone Star College
                  </h4>
                  <p class="text-sm text-slate-600 dark:text-slate-400 mb-3">2023 – 2024</p>
                  <div class="pl-5 mt-3">
                    <div class="text-gray-700 dark:text-gray-300 mb-1">• Dual coursework: Web Design and Art Appreciation</div>
                    <div class="text-gray-700 dark:text-gray-300 mb-1">• 4.0 GPA</div>
                    <div class="text-gray-700 dark:text-gray-300">• Completed college-level coursework while in high school</div>
                  </div>
                </div>
              </div>
            </section>
  
            <!-- Extracurricular Activities Section - Without bullets -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Extracurricular Activities
              </h3>
              <div class="pl-5 space-y-2 text-gray-700 dark:text-gray-300">
                <div>• Self-directed learning in data visualization and database tools</div>
                <div>• Brazilian Jiu Jitsu</div>
                <div>• Tae Kwon Do</div>
              </div>
            </section>
  
            <!-- Volunteer Experience Section - Without bullets -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Volunteer Work
              </h3>
              <div class="pl-5 text-gray-700 dark:text-gray-300">
                <div>• Academy 4 Volunteer (2019) - Assisted with packing food for homeless shelters</div>
              </div>
            </section>
  
            <!-- Achievements Section - Without bullets -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Achievements
              </h3>
              <div class="pl-5 space-y-2 text-gray-700 dark:text-gray-300">
                <div>• A Honor Roll Student - 6 consecutive years</div>
                <div>• TSI2 Completion Certificate</div>
                <div>• Udemy Adobe Mastery Certificate</div>
              </div>
            </section>
  
            <!-- Skills Section - Without bullets -->
            <section>
              <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6 border-l-4 border-slate-700 dark:border-slate-500 pl-4">
                Skills
              </h3>
              <div class="pl-5 space-y-2 text-gray-700 dark:text-gray-300">
                <div>• Coding (Nuxt.js, Vue 3, HTML, CSS)</div>
                <div>• Data Science & Analytics (collecting, organizing, and analyzing data)</div>
                <div>• Database Organization (Notion.so)</div>
              </div>
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
            <!-- <div class="text-center">
              <UButton
                label="Download Full Resume (PDF)"
                icon="i-lucide-download"
                to="/Roman-Ross-Resume.pdf"
                color="gray"
                class="bg-slate-800 hover:bg-slate-700 dark:bg-slate-700 dark:hover:bg-slate-600 text-white font-medium"
              />
            </div> -->
          </div>
        </div>
      </div>
    </section>
  </template>