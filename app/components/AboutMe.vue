<template>
  <section id="about" class="relative overflow-hidden py-20 px-6 max-w-5xl mx-auto">
    
    <!-- Modern Matrix Background -->
    <div class="absolute inset-0 -z-10 transition-opacity duration-1000" :class="{ 'opacity-0': faded }">
      <canvas ref="matrixCanvas" class="w-full h-full"></canvas>
    </div>

    <!-- Main Content -->
    <div class="grid grid-cols-1 md:grid-cols-12 gap-8 animate-fade-in-up relative z-10">
      <!-- Left side with heading -->
      <div class="md:col-span-4 text-left">
        <h2 class="text-5xl font-bold text-gray-900 dark:text-white leading-tight tracking-tight mb-4">
          About<br>Me
        </h2>
      </div>
      
      <!-- Right side with content -->
      <div class="md:col-span-8 text-left">
        <p class="text-lg text-gray-600 dark:text-gray-300 border-l-4 border-teal-500 dark:border-teal-400 pl-5 py-2">
          Hi, I'm <span class="font-semibold text-teal-600 dark:text-teal-400">Roman Ross</span>, a student focused on coding, data science, and web design, with a strong interest in science and communication. I'm currently seeking opportunities to grow and contribute, and I look forward to exploring creative work through YouTube.
        </p>
      </div>
    </div>

  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'

const matrixCanvas = ref(null)
const faded = ref(false)

onMounted(() => {
  const canvas = matrixCanvas.value
  const ctx = canvas.getContext('2d')

  // Set canvas to full size
  canvas.width = window.innerWidth
  canvas.height = window.innerHeight

  const letters = "アァイィウエェオカキクケコサシスセソタチツテトナニヌネノABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789".split("")
  const fontSize = 14
  const columns = Math.floor(canvas.width / fontSize)
  const drops = Array.from({ length: columns }).fill(1)

  function draw() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)" // Subtle fade effect
    ctx.fillRect(0, 0, canvas.width, canvas.height)

    ctx.fillStyle = "rgba(20, 184, 166, 0.7)" // Stronger teal, more visible
    ctx.font = `${fontSize}px monospace`

    for (let i = 0; i < drops.length; i++) {
      const text = letters[Math.floor(Math.random() * letters.length)]
      ctx.fillText(text, i * fontSize, drops[i] * fontSize)

      if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
        drops[i] = 0
      }

      drops[i]++
    }
  }

  const intervalId = setInterval(draw, 50)

  setTimeout(() => {
    faded.value = true           // Trigger fade out animation
    setTimeout(() => {
      clearInterval(intervalId)    // Stop drawing
      ctx.clearRect(0, 0, canvas.width, canvas.height) // Clear the final frame
    }, 1000)
  }, 8000)

  window.addEventListener('resize', () => {
    canvas.width = window.innerWidth
    canvas.height = window.innerHeight
  })
})
</script>

<style scoped>
canvas {
  display: block;
  background: transparent;
}

/* Fade out class */
.opacity-0 {
  opacity: 0;
}

/* Animation */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fadeInUp 0.8s ease-out forwards;
}
</style>