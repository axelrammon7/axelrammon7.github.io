<script setup lang="ts">
</script>

<template>
  <section id="about" class="section-padding bg-white">
    <div class="grid md:grid-cols-2 gap-16 items-center">
      <!-- Image/Visual Side -->
      <div class="relative order-2 md:order-1">
         <div class="aspect-[4/5] bg-stone-100 rounded-2xl overflow-hidden relative">
             <!-- Abstract nature shape or placeholder -->
             <div class="absolute inset-0 flex items-center justify-center text-stone-300">
                <svg width="100" height="100" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22v-9"/><path d="M12 13V8"/><path d="M12 2v2"/><path d="M2.05 15a10 10 0 0 1 19.9 0"/></svg>
             </div>
         </div>
      </div>

      <!-- Text Side -->
      <div class="order-1 md:order-2">
        <h2 class="text-4xl font-display font-medium mb-8 text-text">About Me</h2>
        <div class="space-y-6 text-secondary text-lg leading-relaxed font-light">
          <p>
            I am a Full Stack Developer with 4 years of experience, balancing technical precision with creative problem-solving. My journey has taken me from building reservation systems to optimizing high-traffic CRMs.
          </p>
          <p>
            With a solid foundation in traditional backend technologies like Java (Spring Boot) and modern frontend frameworks like React and Nuxt, I aim to create software that feels natural and intuitive.
          </p>
          <p>
            Currently, I am looking to expand my expertise in cloud architecture (AWS) and python-based solutions, always striving for cleaner, more efficient code.
          </p>
        </div>
        
        <div class="mt-12 flex gap-12 border-t border-stone-100 pt-8">
           <div>
              <h3 class="text-3xl font-display font-medium text-text mb-1">4+</h3>
              <p class="text-sm text-secondary uppercase tracking-widest">Years</p>
           </div>
           <div>
              <h3 class="text-3xl font-display font-medium text-text mb-1">10+</h3>
              <p class="text-sm text-secondary uppercase tracking-widest">Projects</p>
           </div>
        </div>
      </div>
    </div>
  </section>
</template>
