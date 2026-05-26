<script setup lang="ts">
import { RouterView } from 'vue-router'
import { Header } from '@/widgets/header'
import { Footer } from '@/widgets/footer'
</script>

<template>
  <div class="flex flex-col min-h-screen bg-[#0b0f19] text-slate-100 overflow-x-hidden antialiased selection:bg-indigo-500 selection:text-white">
    <Header />
    <main class="flex-grow">
      <RouterView />
    </main>
    <Footer />
  </div>
</template>
