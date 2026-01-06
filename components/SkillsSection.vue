<script setup lang="ts">
import { Code2, Database, Layout, Server, Boxes, Cloud } from 'lucide-vue-next'

const skillCategories = [
  {
    title: 'Frontend',
    icon: Layout,
    skills: ['React', 'TypeScript', 'Vue.js / Nuxt 3', 'Tailwind CSS', 'Pinia', 'SASS']
  },
  {
    title: 'Backend',
    icon: Server,
    skills: ['Java (Spring Boot)', 'Python', 'REST APIs', 'Laravel', 'Node.js']
  },
  {
    title: 'DevOps & Tools',
    icon: Boxes,
    skills: ['Docker', 'Git / Bitbucket', 'CI/CD (Basic)', 'Jira', 'Postman', 'Linux']
  },
  {
    title: 'Cloud & Database',
    icon: Cloud,
    skills: ['AWS (Lambda/SQS Interest)', 'H2 Database', 'PostgreSQL', 'MySQL']
  }
]
</script>

<template>
  <section id="skills" class="section-padding bg-[#fafaf9]">
    <div class="mb-16 max-w-2xl">
      <h2 class="text-3xl md:text-5xl font-display font-medium mb-6 text-text">Technical Skills</h2>
      <p class="text-secondary text-lg font-light">
        A comprehensive toolset allowing me to build scalable, resilient, and user-friendly digital products.
      </p>
    </div>

    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
      <div 
        v-for="(category, index) in skillCategories" 
        :key="category.title"
        class="nature-card group hover:-translate-y-1 transition-transform duration-300"
      >
        <div class="w-10 h-10 bg-primary/10 rounded-full flex items-center justify-center mb-6 text-primary group-hover:bg-primary group-hover:text-white transition-colors duration-300">
          <component :is="category.icon" class="w-5 h-5" />
        </div>
        
        <h3 class="text-xl font-display font-medium mb-4 text-text">{{ category.title }}</h3>
        
        <ul class="space-y-3">
          <li v-for="skill in category.skills" :key="skill" class="flex items-center gap-3 text-secondary text-sm">
            <span class="w-1.5 h-1.5 rounded-full bg-stone-300 group-hover:bg-primary/50 transition-colors"></span>
            {{ skill }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
