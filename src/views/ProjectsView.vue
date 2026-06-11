<template>
  <div class="projects container mx-auto px-6 py-16 max-w-4xl">
    <h1 class="font-display text-4xl text-zinc-100 mb-12" v-scroll-animation>Selected Work</h1>
    <div class="grid md:grid-cols-2 gap-6">
      <div v-for="project in projects" :key="project.id"
           class="bg-white/5 backdrop-blur rounded-2xl ring-1 ring-white/10 p-6 hover:ring-gold-400/40 transition duration-300 flex flex-col"
           v-scroll-animation>
        <h2 class="font-display text-2xl text-zinc-100 mb-2">{{ project.name }}</h2>
        <p class="text-sm text-zinc-400 leading-relaxed mb-4">{{ project.description }}</p>
        <ul class="space-y-1.5 text-sm text-zinc-400 list-disc list-inside mb-6 flex-grow">
          <li v-for="(feature, index) in project.features" :key="index">{{ feature }}</li>
        </ul>
        <div>
          <a v-if="project.link" :href="project.link" target="_blank" rel="noopener"
             class="text-gold-300 hover:text-gold-400 text-sm font-medium transition-colors">
            {{ project.linkLabel }} →
          </a>
          <span v-else class="text-xs uppercase tracking-wider text-zinc-500">Private / client engagement</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectsView',
  data() {
    return {
      projects: [
        {
          id: 1,
          name: 'Enterprise MCP Servers',
          description: 'Model Context Protocol servers that let AI agents operate enterprise platforms safely.',
          features: [
            'Integrations for QuickBooks, Bloomberg, and productivity SaaS tools',
            'OAuth 2.0 and token-based authentication throughout',
            'Built for audit traceability in regulated environments'
          ],
          link: null
        },
        {
          id: 2,
          name: 'Near-Autonomous Delivery Pipeline',
          description: 'An AI-driven software delivery pipeline that takes work from requirements to deployment with minimal human intervention.',
          features: [
            'Requirements decomposition and AI code generation',
            'Automated testing and deployment orchestration',
            'Agentic workflows built on Claude Code'
          ],
          link: null
        },
        {
          id: 3,
          name: 'jaredwienen.com',
          description: 'This site — a Vue 3 single-page portfolio with Tailwind CSS, deployed on Netlify.',
          features: [
            'Vue 3 composition API with Vue Router',
            'Custom dark design system with Tailwind',
            'Continuous deployment from GitHub'
          ],
          link: 'https://github.com/SovereignWave/resume',
          linkLabel: 'View on GitHub'
        },
        {
          id: 4,
          name: 'Operational Tooling Suite',
          description: 'Internal tools built on the job at Amazon and Google Fiber that automated daily operations.',
          features: [
            'Routing and calculation tools in Python and Java',
            'QA databases and knowledge base systems',
            'Browser automation with JavaScript (Tampermonkey)'
          ],
          link: null
        }
      ]
    }
  }
}
</script>
