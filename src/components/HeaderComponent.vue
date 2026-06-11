<template>
  <header class="sticky top-0 z-50 backdrop-blur-md bg-ink-950/80 border-b border-white/5">
    <div class="container mx-auto px-6 py-4 flex justify-between items-center">
      <router-link to="/" class="font-display text-xl tracking-wide text-zinc-100">
        Jared <span class="text-gold-400">Wienen</span>
      </router-link>
      <nav class="flex items-center">
        <button @click="toggleMenu" class="md:hidden focus:outline-none text-zinc-300" aria-label="Toggle menu">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!menuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 6h16M4 12h16M4 18h16"></path>
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
        <ul :class="{'hidden': !menuOpen}" class="md:flex absolute md:static top-full left-0 right-0 bg-ink-900 md:bg-transparent px-6 py-4 md:p-0 space-y-3 md:space-y-0 md:space-x-8 text-sm tracking-wide uppercase">
          <li v-for="item in menuItems" :key="item.route">
            <router-link :to="item.route" class="text-zinc-400 hover:text-gold-300 transition-colors duration-200" active-class="text-gold-400" @click="closeMenu">
              {{ item.name }}
            </router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'HeaderComponent',
  setup() {
    const menuOpen = ref(false)
    const menuItems = [
      { name: 'Home', route: '/' },
      { name: 'Experience', route: '/experience' },
      { name: 'Projects', route: '/projects' },
      { name: 'Skills', route: '/skills' },
      { name: 'Education', route: '/education' },
      { name: 'About', route: '/about' },
      { name: 'Contact', route: '/contact' },
    ]
    const toggleMenu = () => { menuOpen.value = !menuOpen.value }
    const closeMenu = () => { menuOpen.value = false }
    return { menuOpen, menuItems, toggleMenu, closeMenu }
  }
}
</script>
