<script setup lang="ts">
import { ArrowRight, Download } from 'lucide-vue-next'
</script>

<template>
  <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden pt-20 bg-[#fafaf9]">
    
    <div class="container mx-auto px-6 relative z-10">
      <div class="max-w-4xl mx-auto text-center">
        
        <h1 class="text-5xl md:text-7xl lg:text-8xl font-display font-medium mb-8 text-text leading-tight animate-slide-up" style="animation-delay: 0.1s">
          Welcome<br />
          <span class="text-secondary italic">to my portfolio</span>
        </h1>

        <p class="text-xl md:text-2xl text-secondary max-w-2xl mx-auto mb-12 font-light leading-relaxed animate-slide-up" style="animation-delay: 0.2s">
          I'm Axel Rammon, a Full Stack Developer. I build clean, efficient, and user-centric applications using Python, Java, and React.
        </p>

        <div class="flex flex-col sm:flex-row items-center justify-center gap-6 animate-slide-up" style="animation-delay: 0.3s">
          <a href="#projects" class="group relative px-8 py-4 bg-text text-white rounded-full font-medium hover:bg-stone-800 transition-all flex items-center gap-3">
            Selected Work
            <ArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
          </a>
        </div>
        
        <!-- Subtle Decor -->
        <div class="mt-24 flex justify-center gap-12 opacity-40 grayscale animate-fade-in" style="animation-delay: 0.5s">
           <div class="w-px h-24 bg-gradient-to-b from-stone-300 to-transparent"></div>
        </div>
      </div>
    </div>
  </section>
</template>
