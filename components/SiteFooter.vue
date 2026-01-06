<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="py-24 bg-[#fafaf9] border-t border-stone-200">
    <div class="container mx-auto px-6 text-center">
      
      <div class="flex justify-center gap-8 text-sm font-medium text-secondary mb-12">
        <a href="#home" class="hover:text-primary transition-colors">Home</a>
        <a href="#about" class="hover:text-primary transition-colors">About</a>
        <a href="#projects" class="hover:text-primary transition-colors">Projects</a>
      </div>

      <div class="text-sm text-stone-400 font-light">
        &copy; {{ currentYear }} Axel Rammon
      </div>
    </div>
  </footer>
</template>
