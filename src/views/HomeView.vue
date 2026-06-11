<template>
  <div class="home">
    <section class="container mx-auto px-6 pt-24 pb-20 text-center">
      <p class="text-gold-400 uppercase tracking-[0.3em] text-xs mb-6" v-scroll-animation>Software Engineer</p>
      <h1 class="font-display text-5xl md:text-7xl font-medium text-zinc-100 mb-8" v-scroll-animation>
        Jared Wienen
      </h1>
      <p class="max-w-2xl mx-auto text-lg text-zinc-400 leading-relaxed mb-12" v-scroll-animation>
        Seven-plus years of professional programming across web development, AI-driven engineering,
        and production internal tooling — building near-autonomous delivery pipelines, MCP server
        integrations, and AI-native solutions for top FAANG companies.
      </p>
      <div class="flex justify-center space-x-4" v-scroll-animation>
        <a href="https://linkedin.com/in/jaredwienen" target="_blank" rel="noopener"
           class="bg-gold-400 hover:bg-gold-300 text-ink-950 font-semibold py-3 px-8 rounded-full transition duration-300">
          Connect on LinkedIn
        </a>
        <router-link to="/experience"
           class="border border-white/15 hover:border-gold-400 text-zinc-200 font-semibold py-3 px-8 rounded-full transition duration-300">
          View Experience
        </router-link>
      </div>
    </section>

    <section class="container mx-auto px-6 pb-24">
      <h2 class="font-display text-3xl text-center text-zinc-100 mb-12" v-scroll-animation>What I Build</h2>
      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div v-for="(service, index) in services" :key="index"
             class="bg-white/5 backdrop-blur rounded-2xl ring-1 ring-white/10 p-6 hover:ring-gold-400/40 transition duration-300"
             v-scroll-animation>
          <component :is="service.icon" class="w-8 h-8 text-gold-400 mb-4" />
          <h3 class="font-display text-xl text-zinc-100 mb-2">{{ service.title }}</h3>
          <p class="text-sm text-zinc-400 leading-relaxed">{{ service.description }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ref } from 'vue'
import { CodeBracketIcon, CpuChipIcon, ServerStackIcon, BoltIcon } from '@heroicons/vue/24/outline'

export default {
  name: 'HomeView',
  components: { CodeBracketIcon, CpuChipIcon, ServerStackIcon, BoltIcon },
  setup() {
    const services = ref([
      {
        title: 'MCP Server Integrations',
        description: 'Model Context Protocol servers connecting AI agents to enterprise platforms with OAuth 2.0-secured APIs.',
        icon: ServerStackIcon
      },
      {
        title: 'Agentic AI Workflows',
        description: 'Near-autonomous delivery pipelines — requirements decomposition, code generation, testing, and deployment.',
        icon: CpuChipIcon
      },
      {
        title: 'Full-Stack Web Apps',
        description: 'React, Vue, and Node applications with clean architecture and responsive, accessible interfaces.',
        icon: CodeBracketIcon
      },
      {
        title: 'Process Automation',
        description: 'Internal tooling in Python, Java, and JavaScript that removes manual work from real operations.',
        icon: BoltIcon
      }
    ])
    return { services }
  }
}
</script>
