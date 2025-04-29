<script setup>
import { ref, onMounted, nextTick } from 'vue'

const projects = [
  { title: 'CSS Code Visualizer', description: 'Visualizes code structure using animation.', type: 'code' },
  { title: 'Purple Star', description: 'A stylized, digital moving star concept.', type: 'art' },
  { title: 'Water Analysis', description: 'Simulates particles in fluid.', type: 'science' },
  { title: 'Signal Pulse', description: 'Sound-reactive visual pulse.', type: 'music' },
  { title: 'Urban Flash', description: 'Mimics shutter blink or flash.', type: 'photo' }
]

function setupCanvas(canvas, type) {
  if (!canvas) return
  nextTick(() => {
    const ctx = canvas.getContext('2d')
    const w = canvas.width = canvas.offsetWidth
    const h = canvas.height = canvas.offsetHeight

    if (type === 'code') {
      let text = '> npm run build\n> Compiling...\n> Done.'
      let index = 0
      function drawTyping() {
        ctx.fillStyle = 'black'
        ctx.fillRect(0, 0, w, h)
        ctx.fillStyle = '#0f0'
        ctx.font = '14px monospace'
        ctx.fillText(text.slice(0, index), 10, 30)
        index = index < text.length ? index + 1 : text.length
        requestAnimationFrame(drawTyping)
      }
      drawTyping()
    }

    if (type === 'art') {
      let t = 0
      function drawCreature() {
        t += 0.01
        ctx.clearRect(0, 0, w, h)
        ctx.beginPath()
        ctx.moveTo(w / 2, h / 2)
        for (let i = 0; i < 360; i++) {
          const angle = i * (Math.PI / 180)
          const radius = 30 + 10 * Math.sin(t * 3 + angle * 5)
          const x = w / 2 + radius * Math.cos(angle)
          const y = h / 2 + radius * Math.sin(angle)
          ctx.lineTo(x, y)
        }
        ctx.closePath()
        ctx.strokeStyle = '#9f7aea'
        ctx.stroke()
        requestAnimationFrame(drawCreature)
      }
      drawCreature()
    }

    if (type === 'science') {
      const orbs = Array.from({ length: 10 }, (_, i) => ({
        angle: Math.random() * Math.PI * 2,
        radius: 30 + i * 5,
        speed: 0.01 + i * 0.002
      }))
      function drawOrbits() {
        ctx.fillStyle = 'black'
        ctx.fillRect(0, 0, w, h)
        ctx.translate(w / 2, h / 2)
        for (const orb of orbs) {
          orb.angle += orb.speed
          const x = orb.radius * Math.cos(orb.angle)
          const y = orb.radius * Math.sin(orb.angle)
          ctx.beginPath()
          ctx.arc(x, y, 2, 0, Math.PI * 2)
          ctx.fillStyle = '#3b82f6'
          ctx.fill()
        }
        ctx.setTransform(1, 0, 0, 1, 0, 0)
        requestAnimationFrame(drawOrbits)
      }
      drawOrbits()
    }

    if (type === 'music') {
      let t = 0
      function drawWave() {
        t += 0.05
        ctx.clearRect(0, 0, w, h)
        ctx.beginPath()
        for (let x = 0; x < w; x++) {
          const y = h / 2 + Math.sin(x * 0.05 + t) * 20
          ctx.lineTo(x, y)
        }
        ctx.strokeStyle = '#f43f5e'
        ctx.lineWidth = 2
        ctx.stroke()
        requestAnimationFrame(drawWave)
      }
      drawWave()
    }

    if (type === 'photo') {
      let alpha = 1
      let fading = true
      function shutterEffect() {
        ctx.clearRect(0, 0, w, h)
        ctx.fillStyle = `rgba(255,255,255,${alpha})`
        ctx.fillRect(0, 0, w, h)
        if (fading) {
          alpha -= 0.1
          if (alpha <= 0) {
            alpha = 0
            fading = false
            setTimeout(() => {
              alpha = 1
              fading = true
            }, 2000 + Math.random() * 3000)
          }
        }
        requestAnimationFrame(shutterEffect)
      }
      shutterEffect()
    }
  })
}
</script>

<template>
  <USection id="projects" padding="py-16" bg-white dark:bg-gray-900>
    <UContainer size="xl">
      <div class="text-center mb-12">
        <USpan class="text-sm font-medium uppercase tracking-wider text-gray-500 dark:text-gray-400 mb-1">
          Portfolio
        </USpan>
        <h2 class="text-2xl font-bold text-gray-800 dark:text-white mb-2">My Projects</h2>
        <div class="w-16 h-1 bg-gray-700 dark:bg-gray-500 mx-auto"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
        <div
          v-for="(project, i) in projects"
          :key="i"
          class="rounded-xl overflow-hidden shadow-md bg-white dark:bg-gray-900 hover:scale-[1.02] transition-transform duration-300 h-full"
        >
          <div class="relative h-48 border-4 border-white dark:border-gray-800 rounded-sm overflow-hidden">
            <canvas
              :ref="el => setupCanvas(el, project.type)"
              class="w-full h-full block"
            ></canvas>
          </div>

          <div class="p-6">
            <h3 class="text-2xl font-bold mb-2 text-gray-900 dark:text-white">{{ project.title }}</h3>
            <p class="text-gray-600 dark:text-gray-300">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </UContainer>
  </USection>
</template>

<style scoped>
.section-title {
  font-size: 1.25rem;
  font-weight: bold;
  padding-left: 1rem;
  border-left: 4px solid #374151;
  margin-bottom: 1rem;
  color: #1f2937;
}
.dark .section-title {
  color: #ffffff;
  border-color: #9ca3af;
}
</style>