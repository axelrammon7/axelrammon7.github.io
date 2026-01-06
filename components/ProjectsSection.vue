<script setup lang="ts">
import { Github, ArrowUpRight } from 'lucide-vue-next'

const projects = [
  {
    title: 'Java Ecosystem Study API',
    description: 'A dedicated study project exploring the Spring Boot ecosystem. Implements a robust REST API for user and task management, featuring persistence via JPA/Hibernate and an H2 in-memory database for rapid prototyping.',
    tags: ['Java', 'Spring Boot', 'JPA', 'H2', 'REST'],
    github: 'https://github.com/axelrammon7/first',
    // Using a more abstract/natural placeholder if possible, or keeping the clean look
    image: 'https://images.unsplash.com/photo-1623479322729-28b25c16b011?q=80&w=2070&auto=format&fit=crop' 
  }
]
</script>

<template>
  <section id="projects" class="section-padding bg-[#fafaf9]">
    <div class="mb-16 max-w-2xl">
      <h2 class="text-3xl md:text-5xl font-display font-medium mb-6 text-text">Selected Projects</h2>
      <p class="text-secondary text-lg font-light">
        Highlights of my technical explorations and open source contributions.
      </p>
    </div>

    <div class="space-y-16">
      <div 
        v-for="(project, index) in projects" 
        :key="project.title" 
        class="group grid md:grid-cols-12 gap-8 items-center"
      >
        <!-- Project Image -->
        <div class="md:col-span-7 relative overflow-hidden rounded-xl bg-stone-200 aspect-video group-hover:shadow-lg transition-all duration-500">
           <img 
             :src="project.image" 
             :alt="project.title"
             class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105 filter grayscale hover:grayscale-0"
           />
           <div class="absolute inset-0 bg-stone-900/10 group-hover:bg-transparent transition-colors"></div>
        </div>
        
        <!-- Project Info -->
        <div class="md:col-span-5 md:-ml-12 relative z-10">
          <div class="nature-card">
              <h3 class="text-2xl font-display font-medium mb-4 text-text">{{ project.title }}</h3>
              
              <p class="text-stone-600 mb-6 leading-relaxed text-sm">
                {{ project.description }}
              </p>
              
              <div class="flex flex-wrap gap-2 mb-8">
                <span 
                  v-for="tag in project.tags" 
                  :key="tag" 
                  class="px-3 py-1 rounded-full text-xs font-medium bg-stone-100 text-stone-600 border border-stone-200"
                >
                  {{ tag }}
                </span>
              </div>

              <div class="flex items-center gap-6">
                <a 
                  :href="project.github" 
                  target="_blank"
                  class="flex items-center gap-2 text-sm font-semibold text-text hover:text-primary transition-colors"
                >
                  <Github class="w-4 h-4" />
                  Source Code
                </a>
              </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
