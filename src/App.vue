<template>
  <div id="app" class="min-h-screen flex flex-col bg-ink-950 text-zinc-200 font-sans antialiased selection:bg-gold-400 selection:text-ink-950">
    <HeaderComponent />
    <main class="flex-grow">
      <router-view v-slot="{ Component }">
        <transition name="fade" mode="out-in">
          <component :is="Component" />
        </transition>
      </router-view>
    </main>
    <footer class="border-t border-white/5 py-8 text-center text-sm text-zinc-500">
      <div class="flex justify-center space-x-6 mb-3">
        <a href="https://linkedin.com/in/jaredwienen" target="_blank" rel="noopener" class="hover:text-gold-300 transition-colors">LinkedIn</a>
        <a href="https://github.com/SovereignWave" target="_blank" rel="noopener" class="hover:text-gold-300 transition-colors">GitHub</a>
      </div>
      <p>&copy; {{ new Date().getFullYear() }} Jared Wienen</p>
    </footer>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  name: 'App',
  components: { HeaderComponent }
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.4s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
