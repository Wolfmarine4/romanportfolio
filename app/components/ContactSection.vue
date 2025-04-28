<template>
  <!-- Contact Section -->
  <section id="contact" class="py-20 bg-white dark:bg-gray-900">
    <div class="container mx-auto px-4">
      <div class="max-w-4xl mx-auto">
        <!-- Section Header -->
        <div class="text-center mb-16">
          <span class="inline-block text-sm font-medium uppercase tracking-wider text-slate-600 dark:text-slate-400 mb-2">
            Get in Touch
          </span>
          <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Let's Connect
          </h2>
          <div class="w-16 h-1 bg-slate-700 dark:bg-slate-500 mx-auto"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-5 gap-8">
          <!-- Contact Information -->
          <div class="md:col-span-2 bg-gray-50 dark:bg-gray-800 border border-gray-200 dark:border-gray-700 p-8 rounded shadow-sm">
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6">
              Contact Information
            </h3>

            <div class="space-y-6 text-gray-700 dark:text-gray-300">
              <div class="flex items-start">
                <div class="flex-shrink-0 w-10 h-10 bg-slate-100 dark:bg-slate-800 rounded-sm flex items-center justify-center mr-4">
                  <Icon name="lucide:mail" class="text-slate-700 dark:text-slate-300 w-6 h-6" />
                </div>
                <div>
                  <p class="font-medium mb-1">Email</p>
                  <a href="mailto:roman.ross@example.com" class="hover:text-slate-800 dark:hover:text-slate-200">
                    roman.ross@example.com
                  </a>
                </div>
              </div>

              <div class="flex items-start">
                <div class="flex-shrink-0 w-10 h-10 bg-slate-100 dark:bg-slate-800 rounded-sm flex items-center justify-center mr-4">
                  <Icon name="lucide:map-pin" class="text-slate-700 dark:text-slate-300 w-6 h-6" />
                </div>
                <div>
                  <p class="font-medium mb-1">Location</p>
                  <span>Dallas, Texas</span>
                </div>
              </div>

              <div class="flex items-start">
                <div class="flex-shrink-0 w-10 h-10 bg-slate-100 dark:bg-slate-800 rounded-sm flex items-center justify-center mr-4">
                  <Icon name="lucide:calendar" class="text-slate-700 dark:text-slate-300 w-6 h-6" />
                </div>
                <div>
                  <p class="font-medium mb-1">Education</p>
                  <span>Class of 2025</span>
                </div>
              </div>
            </div>

            <!-- Social Media Links -->
            <div class="mt-8">
              <p class="font-medium text-gray-900 dark:text-white mb-4">
                Follow Me
              </p>
              <div class="flex space-x-4">
                <a href="https://instagram.com/romanross" target="_blank" class="w-10 h-10 bg-slate-100 dark:bg-slate-800 flex items-center justify-center rounded-sm hover:bg-slate-200 dark:hover:bg-slate-700 transition-colors">
                  <Icon name="simple-icons:instagram" class="text-slate-700 dark:text-slate-300 w-6 h-6" />
                </a>
                <a href="https://github.com/WolfMarine4" target="_blank" class="w-10 h-10 bg-slate-100 dark:bg-slate-800 flex items-center justify-center rounded-sm hover:bg-slate-200 dark:hover:bg-slate-700 transition-colors">
                  <Icon name="simple-icons:github" class="text-slate-700 dark:text-slate-300 w-6 h-6" />
                </a>
              </div>
            </div>
          </div>

          <!-- Contact Form Area -->
          <!-- <div class="md:col-span-3 bg-gray-50 dark:bg-gray-800 border border-gray-200 dark:border-gray-700 p-8 rounded shadow-sm">
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-6">
              Send a Message
            </h3>
            <p class="text-gray-700 dark:text-gray-300 mb-8">
              Interested in collaborating or have questions about my work? I'm always open to new opportunities and connections.
            </p>
            <div class="space-y-6">
              <UButton
                block
                color="gray"
                to="mailto:roman.ross@example.com"
                icon="i-lucide-mail"
                label="Email Me"
                class="bg-slate-800 hover:bg-slate-700 dark:bg-slate-700 dark:hover:bg-slate-600 text-white font-medium"
              />
              <UButton
                block
                to="#resume"
                trailing-icon="i-lucide-file-text"
                label="Download Resume"
                variant="outline"
                color="gray"
                class="border-slate-600 dark:border-slate-400 text-slate-800 dark:text-slate-200 font-medium"
              />
            </div> 
          </div> -->
        </div>
      </div>
    </div>
  </section>
</template>
