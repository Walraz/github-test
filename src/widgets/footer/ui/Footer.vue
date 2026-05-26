<template>
  <footer class="w-full border-t border-slate-800/60 bg-[#070b13] py-8 text-slate-500 text-sm">
    <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-4">
      <div class="flex items-center gap-2">
        <div class="w-6 h-6 rounded-md bg-gradient-to-tr from-indigo-500 to-purple-600 flex items-center justify-center text-white font-bold text-xs">
          gt
        </div>
        <span class="font-semibold text-slate-300">github test</span>
      </div>
      
      <p class="text-center md:text-left text-xs text-slate-600">
        &copy; {{ new Date().getFullYear() }} github test. Built with Vue 3, Vite, Tailwind CSS, and FSD.
      </p>

      <div class="flex items-center gap-6 text-xs text-slate-400">
        <a href="https://feature-sliced.design/" target="_blank" class="hover:text-white transition-colors">FSD Spec</a>
        <a href="https://github.com" target="_blank" class="hover:text-white transition-colors">GitHub</a>
        <a href="https://vuejs.org/" target="_blank" class="hover:text-white transition-colors">Vue Docs</a>
      </div>
    </div>
  </footer>
</template>
