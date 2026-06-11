<template>
  <div class="contact container mx-auto px-6 py-24 max-w-2xl text-center">
    <h1 class="font-display text-4xl text-zinc-100 mb-6" v-scroll-animation>Get in Touch</h1>
    <p class="text-zinc-400 leading-relaxed mb-12" v-scroll-animation>
      The fastest way to reach me is through LinkedIn — I respond to messages there daily.
      You can also find my open-source work on GitHub.
    </p>
    <div class="flex justify-center space-x-4" v-scroll-animation>
      <a href="https://linkedin.com/in/jaredwienen" target="_blank" rel="noopener"
         class="bg-gold-400 hover:bg-gold-300 text-ink-950 font-semibold py-3 px-8 rounded-full transition duration-300">
        Message on LinkedIn
      </a>
      <a href="https://github.com/indohippi" target="_blank" rel="noopener"
         class="border border-white/15 hover:border-gold-400 text-zinc-200 font-semibold py-3 px-8 rounded-full transition duration-300">
        GitHub Profile
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactView'
}
</script>
