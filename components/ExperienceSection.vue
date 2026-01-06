<script setup lang="ts">
const jobs = [
  {
    role: 'Full Stack Developer',
    company: 'EasyRev',
    location: 'Natal',
    period: 'Nov/2024 – Jul/2025',
    description: 'Acted in the full lifecycle of Reservation Management (RMS) and Property Management (PMS) systems.',
    achievements: [
      'Developed Backend modules for RESTful APIs and high-performance reactive Frontend.',
      'Implemented payment integrations (Stripe) and critical reservation automation.',
      'Orchestrated dev, staging, and homologation environments using Docker.',
      'Focused on reusable components and UI performance optimization.'
    ]
  },
  {
    role: 'Full Stack Developer',
    company: 'LUA4',
    location: 'Natal',
    period: 'Set/2022 – Mar/2024',
    description: 'Focused on high-traffic vehicle management systems and CRM.',
    achievements: [
      'Evolutionary maintenance and refactoring of critical legacy modules.',
      'Improved code performance and maintainability.',
      'Contributed to versioning flow (Git/Bitbucket) and agile task management (Jira).',
      'Worked with build tools and automation (Gulp.js, SASS).'
    ]
  },
  {
    role: 'Front End Developer',
    company: 'Braso Soluções Tecnológicas',
    location: 'Natal',
    period: 'Dez/2020 – Mar/2022',
    description: 'Development and maintenance of institutional websites and custom systems.',
    achievements: [
      'Focus on responsive layouts and SEO optimization.',
      'Created content management solutions.',
      'Provided technical support to clients.'
    ]
  }
]
</script>

<template>
  <section id="experience" class="section-padding bg-white">
    <div class="mb-16 max-w-2xl">
      <h2 class="text-3xl md:text-5xl font-display font-medium mb-6 text-text">Experience</h2>
      <p class="text-secondary text-lg font-light">My professional journey in the technology industry.</p>
    </div>

    <div class="max-w-3xl">
      <div class="space-y-12">
        <div 
          v-for="(job, index) in jobs" 
          :key="index"
          class="relative pl-8 border-l border-stone-200"
        >
          <!-- Tiny dot on the timeline -->
          <div class="absolute -left-1.5 top-2 w-3 h-3 rounded-full bg-white border border-stone-300"></div>

          <div class="mb-2">
             <span class="text-sm font-medium text-primary tracking-wide uppercase">{{ job.period }}</span>
          </div>
          
          <h3 class="text-2xl font-display font-medium text-text mb-1">{{ job.role }}</h3>
          <div class="text-lg text-secondary mb-4">{{ job.company }} &middot; {{ job.location }}</div>

          <p class="text-stone-600 mb-6 leading-relaxed">{{ job.description }}</p>

          <ul class="space-y-2">
             <li v-for="(achievement, i) in job.achievements" :key="i" class="flex items-start gap-3 text-stone-500 text-sm">
               <span class="mt-2 w-1 h-1 rounded-full bg-stone-400 flex-shrink-0"></span>
               {{ achievement }}
             </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
