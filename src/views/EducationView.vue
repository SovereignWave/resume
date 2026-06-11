<template>
  <div class="education container mx-auto px-6 py-16 max-w-3xl">
    <h1 class="font-display text-4xl text-zinc-100 mb-12" v-scroll-animation>Education & Certifications</h1>
    <div class="space-y-6 mb-12" v-scroll-animation>
      <div class="bg-white/5 backdrop-blur rounded-2xl ring-1 ring-white/10 p-6">
        <h2 class="font-display text-2xl text-zinc-100">Fullstack Academy</h2>
        <p class="text-sm text-gold-300 mt-1 mb-2">Web Development & Computer Science · February 2023 – October 2023</p>
        <p class="text-sm text-zinc-400">Immersive software engineering program covering full-stack JavaScript, React, Node.js, and computer science fundamentals.</p>
      </div>
      <div class="bg-white/5 backdrop-blur rounded-2xl ring-1 ring-white/10 p-6">
        <h2 class="font-display text-2xl text-zinc-100">Trinity Valley Community College</h2>
        <p class="text-sm text-gold-300 mt-1 mb-2">Associate of Arts, Music Business · 2008 – 2011</p>
      </div>
    </div>
    <h2 class="font-display text-2xl text-zinc-100 mb-6" v-scroll-animation>Certifications</h2>
    <ul class="grid sm:grid-cols-2 gap-3" v-scroll-animation>
      <li v-for="cert in certifications" :key="cert"
          class="bg-white/5 ring-1 ring-white/10 rounded-xl px-4 py-3 text-sm text-zinc-300">
        {{ cert }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'EducationView',
  data() {
    return {
      certifications: [
        'Career Essentials in Software Development — Microsoft & LinkedIn',
        'Web Development — Fullstack Academy',
        'Google Analytics Certification',
        'Google Ads Certification'
      ]
    }
  }
}
</script>
