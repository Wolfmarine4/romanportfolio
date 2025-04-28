<script setup>
defineProps({
  title: String,
  description: String,
  buttonLabel: {
    type: String,
    default: 'View Project'
  }
})
</script>

<template>
  <div class="bg-gray-50 dark:bg-gray-800 rounded overflow-hidden shadow-sm hover:shadow-md transition-shadow">
    <div class="aspect-video bg-gray-200 dark:bg-gray-700"></div>
    <div class="p-6">
      <h4 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">{{ title }}</h4>
      <p class="text-gray-700 dark:text-gray-300 mb-4">{{ description }}</p>
      <UButton
        :label="buttonLabel"
        variant="outline"
        color="gray"
        size="sm"
        class="border-slate-600 dark:border-slate-400 text-slate-800 dark:text-slate-200 font-medium"
      />
    </div>
  </div>
</template>
