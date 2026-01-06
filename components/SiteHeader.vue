<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import { Menu, X, Github, Linkedin, Mail } from 'lucide-vue-next'

const isScrolled = ref(false)
const isMobileMenuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20
}

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const navItems = [
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Skills', href: '#skills' },
  { name: 'Experience', href: '#experience' },
  { name: 'Projects', href: '#projects' },
]

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header 
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-500 ease-in-out"
    :class="[isScrolled ? 'bg-background/90 backdrop-blur-sm border-b border-stone-200 py-4' : 'bg-transparent py-8']"
  >
    <nav class="container mx-auto px-6 flex items-center justify-between">
      <!-- Logo -->
      <a href="#" class="text-2xl font-display font-medium text-text group">
        Axel<span class="text-primary group-hover:text-primary/70 transition-colors">.</span>
      </a>

      <!-- Desktop Nav -->
      <div class="hidden md:flex items-center gap-10">
        <a 
          v-for="item in navItems" 
          :key="item.name" 
          :href="item.href"
          class="text-sm font-medium text-secondary hover:text-primary transition-colors tracking-wide"
        >
          {{ item.name }}
        </a>
      </div>

      <!-- Social Icons (Desktop) -->
      <div class="hidden md:flex items-center gap-4">
        <a href="https://github.com/axelrammon7" target="_blank" class="p-2 text-secondary hover:text-primary hover:bg-stone-100 rounded-full transition-all">
          <Github class="w-5 h-5" />
        </a>
        <a href="https://www.linkedin.com/in/axel-rammon-4493b436b" target="_blank" class="p-2 text-secondary hover:text-primary hover:bg-stone-100 rounded-full transition-all">
          <Linkedin class="w-5 h-5" />
        </a>
        <a href="mailto:axelrammon48@gmail.com" class="p-2 text-secondary hover:text-primary hover:bg-stone-100 rounded-full transition-all">
          <Mail class="w-5 h-5" />
        </a>
      </div>

      <!-- Mobile Menu Button -->
      <button @click="toggleMobileMenu" class="md:hidden p-2 text-text">
        <Menu v-if="!isMobileMenuOpen" class="w-6 h-6" />
        <X v-else class="w-6 h-6" />
      </button>
    </nav>

    <!-- Mobile Nav -->
    <div 
      v-if="isMobileMenuOpen"
      class="md:hidden absolute top-full left-0 right-0 bg-background border-b border-stone-200 p-6 flex flex-col gap-6 shadow-xl"
    >
      <a 
        v-for="item in navItems" 
        :key="item.name" 
        :href="item.href"
        @click="isMobileMenuOpen = false"
        class="text-lg font-medium text-text hover:text-primary"
      >
        {{ item.name }}
      </a>
      <div class="flex items-center gap-6 pt-4 border-t border-stone-100">
        <a href="https://github.com/axelrammon7" target="_blank" class="text-secondary hover:text-primary">
          <Github class="w-6 h-6" />
        </a>
        <a href="https://www.linkedin.com/in/axel-rammon-4493b436b" target="_blank" class="text-secondary hover:text-primary">
          <Linkedin class="w-6 h-6" />
        </a>
         <a href="mailto:axelrammon48@gmail.com" class="text-secondary hover:text-primary">
          <Mail class="w-6 h-6" />
        </a>
      </div>
    </div>
  </header>
</template>
