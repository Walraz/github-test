<script setup lang="ts">
import { ref } from 'vue'

const features = ref([
  {
    title: 'Vite + Vue 3 + TypeScript',
    description: 'Lightning-fast development server with type safety and the reactivity of Vue 3 Composition API.',
    icon: '⚡'
  },
  {
    title: 'Feature-Sliced Design (FSD)',
    description: 'A structural methodology for frontend applications. Scalable, easy to maintain, and highly modular.',
    icon: '🧩'
  },
  {
    title: 'Tailwind CSS Integration',
    description: 'Rapidly style modern web applications with utility classes, fully tailored to support rich aesthetics.',
    icon: '🎨'
  },
  {
    title: 'Vue Router v4',
    description: 'Smooth, seamless client-side navigation with dynamic routing support and page transitions.',
    icon: '🚦'
  }
])

const ctaClicked = () => {
  alert('Thank you for getting started with github test! 🎉')
}
</script>

<template>
  <div class="relative min-h-[calc(100vh-140px)] flex flex-col justify-between overflow-hidden">
    <!-- Ambient Glow Backdrops -->
    <div class="absolute top-1/4 left-1/4 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-indigo-600/10 rounded-full blur-[100px] pointer-events-none"></div>
    <div class="absolute bottom-1/4 right-1/4 translate-x-1/2 translate-y-1/2 w-[450px] h-[450px] bg-purple-600/10 rounded-full blur-[120px] pointer-events-none"></div>
    
    <!-- Grid Overlay -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#ffffff03_1px,transparent_1px),linear-gradient(to_bottom,#ffffff03_1px,transparent_1px)] bg-[size:4rem_4rem] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_40%,#000_70%,transparent_100%)] pointer-events-none"></div>

    <!-- Main Container -->
    <div class="max-w-7xl mx-auto px-6 py-20 relative z-10 flex-grow flex flex-col justify-center items-center">
      <!-- Hero Section -->
      <div class="text-center max-w-3xl mx-auto">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full border border-indigo-500/30 bg-indigo-500/5 text-xs text-indigo-400 font-semibold mb-6 hover:bg-indigo-500/10 transition-colors cursor-pointer">
          <span class="w-1.5 h-1.5 rounded-full bg-indigo-400 animate-pulse"></span>
          Now Live: github test template
        </div>

        <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight text-white mb-6 leading-tight">
          Crafting the Future of <br />
          <span class="bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 via-purple-400 to-pink-500">
            Modular Web Apps
          </span>
        </h1>

        <p class="text-lg md:text-xl text-slate-400 mb-10 leading-relaxed font-light">
          A starter template showcasing the power of Feature-Sliced Design (FSD) coupled with Vite, Vue 3, TypeScript, and Tailwind CSS. Built to scale seamlessly.
        </p>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center mb-24">
          <button 
            @click="ctaClicked"
            class="px-8 py-4 bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-semibold rounded-xl shadow-lg shadow-indigo-500/20 hover:shadow-indigo-500/35 hover:-translate-y-0.5 transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-indigo-400"
          >
            Get Started
          </button>
          
          <a 
            href="https://feature-sliced.design/"
            target="_blank"
            class="px-8 py-4 bg-slate-800/80 border border-slate-700/80 text-slate-300 font-semibold rounded-xl backdrop-blur hover:bg-slate-800 hover:text-white hover:border-slate-600 hover:-translate-y-0.5 transition-all duration-200 flex items-center gap-2"
          >
            Learn FSD Architecture
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
            </svg>
          </a>
        </div>
      </div>

      <!-- Feature Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 w-full mt-8">
        <div 
          v-for="feat in features" 
          :key="feat.title"
          class="group relative bg-slate-900/40 border border-slate-800/80 rounded-2xl p-6 backdrop-blur hover:border-indigo-500/30 hover:bg-slate-900/60 transition-all duration-300 shadow-xl"
        >
          <!-- Accent Gradient border hover -->
          <div class="absolute inset-0 rounded-2xl bg-gradient-to-tr from-indigo-500/10 to-purple-500/0 opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"></div>
          
          <div class="w-12 h-12 rounded-xl bg-slate-800/50 border border-slate-700/50 flex items-center justify-center text-2xl mb-4 group-hover:scale-110 transition-transform duration-300">
            {{ feat.icon }}
          </div>
          
          <h3 class="text-lg font-bold text-slate-200 mb-2 group-hover:text-indigo-300 transition-colors duration-300">
            {{ feat.title }}
          </h3>
          
          <p class="text-sm text-slate-400 leading-relaxed font-light">
            {{ feat.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
