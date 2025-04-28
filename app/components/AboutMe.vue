<template>
    <section id="about" class="relative overflow-hidden py-20 px-6 max-w-5xl mx-auto text-center">
      
      <!-- Modern Matrix Background -->
      <div class="absolute inset-0 -z-10 transition-opacity duration-1000" :class="{ 'opacity-0': faded }">
        <canvas ref="matrixCanvas" class="w-full h-full"></canvas>
      </div>
  
      <!-- Main Content -->
      <div class="flex flex-col items-center space-y-6 animate-fade-in-up relative z-10">
        <h2 class="text-4xl font-bold text-gray-900 dark:text-white leading-tight">
          About Me
        </h2>
  
        <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl">
          Hi, I'm <span class="font-semibold text-teal-600 dark:text-teal-400">Roman Ross</span>, a student focused on coding, data science, and web design, with a strong interest in science and communication. I'm currently seeking opportunities to grow and contribute, and I look foward to exploring creative work through YouTube.
        </p>
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
      ctx.clearRect(0, 0, canvas.width, canvas.height) // Clear without background fill
  
      ctx.fillStyle = "rgba(20, 184, 166, 0.4)" // Stronger teal, more visible
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
      clearInterval(intervalId)    // Stop drawing
      ctx.clearRect(0, 0, canvas.width, canvas.height) // Clear the final frame
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
  </style>
  