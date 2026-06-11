<template>
  <div class="experience container mx-auto px-6 py-16 max-w-4xl">
    <h1 class="font-display text-4xl text-zinc-100 mb-12" v-scroll-animation>Professional Experience</h1>
    <div class="relative border-l border-white/10 ml-3 space-y-10">
      <div v-for="(job, index) in jobs" :key="index" class="relative pl-8" v-scroll-animation>
        <div class="absolute -left-[7px] top-1.5 w-3.5 h-3.5 rounded-full bg-gold-400 ring-4 ring-ink-950"></div>
        <div class="bg-white/5 backdrop-blur rounded-2xl ring-1 ring-white/10 p-6 hover:ring-gold-400/40 transition duration-300">
          <h2 class="font-display text-2xl text-zinc-100">{{ job.title }}</h2>
          <p class="text-sm text-gold-300 mt-1 mb-4">{{ job.company }} · {{ job.location }} · {{ job.period }}</p>
          <ul class="space-y-2 text-sm text-zinc-400 leading-relaxed list-disc list-inside">
            <li v-for="(r, rIndex) in job.responsibilities" :key="rIndex">{{ r }}</li>
          </ul>
          <a v-if="job.link" :href="job.link" target="_blank" rel="noopener" class="inline-block mt-4 text-gold-300 hover:text-gold-400 text-sm font-medium transition-colors">{{ job.linkLabel }} &rarr;</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'ExperienceView',
  setup() {
    const jobs = ref([
      {
        title: 'Software Engineer',
        company: 'Mercor',
        location: 'Remote',
        period: 'February 2025 – Present',
        responsibilities: [
          'Design and develop MCP (Model Context Protocol) servers enabling AI agents to integrate with enterprise platforms including QuickBooks and Bloomberg, secured with OAuth 2.0 and token-based authentication.',
          'Build and validate near-autonomous AI delivery pipelines covering requirements decomposition, code generation, automated testing, and deployment orchestration.',
          'Engineer agentic workflows using Claude Code, applying prompt engineering and AI-assisted debugging to accelerate delivery velocity.',
          'Selected for the contractor review team within weeks of starting; lead projects and contribute to team-wide quality guidelines.'
        ],
        link: 'https://www.mercor.com/stories/jared/',
        linkLabel: 'Watch the Mercor spotlight interview'
      },
      {
        title: 'Software Engineer — AI Model Evaluation (Contract)',
        company: 'TELUS Digital',
        location: 'Austin, TX',
        period: 'August 2024 – Present',
        responsibilities: [
          'Contract software engineering within AI training programs for top AI companies, delivered in regulated, confidentiality-bound environments.',
          'Review, evaluate, and refine AI-generated outputs including PhD-level math reasoning annotations to improve model accuracy.',
          'Develop evaluation and integration tooling under strict security and access-control requirements.'
        ]
      },
      {
        title: 'Web Developer',
        company: 'Heavenly Wave',
        location: 'Austin, TX',
        period: 'February 2022 – Present',
        responsibilities: [
          'Led AI development projects for top FAANG companies focused on intelligent solution design and AI-native interfaces.',
          'Architected full-stack web solutions in React and JavaScript for clients from personal networks to enterprise organizations.',
          'Developed RESTful APIs and integrated third-party services for seamless system interoperability.'
        ]
      },
      {
        title: 'AI Software Developer',
        company: 'Remotasks',
        location: 'Remote',
        period: 'April 2023 – August 2023',
        responsibilities: [
          'Developed, evaluated, and refined AI-generated code using agentic workflows, improving model accuracy and output quality.',
          'Assessed AI toolchains and emerging methodologies, providing structured feedback across software delivery tasks.'
        ]
      },
      {
        title: 'Logistics Engineer',
        company: 'Amazon',
        location: 'Austin, TX',
        period: 'July 2022 – March 2024',
        responsibilities: [
          'Developed routing and automation tools in Python and Java for operational workflows in a high-scale distributed environment.',
          'Built routing analytics and data pipelines with Tableau and Python.',
          'Owned outcomes end-to-end under Amazon Single Threaded Owner principles.'
        ]
      },
      {
        title: 'Technical Support Engineer',
        company: 'OneSupport (Google Fiber)',
        location: 'Austin, TX',
        period: 'October 2018 – August 2022',
        responsibilities: [
          'Built and deployed internal tooling — routing tools, QA databases, and knowledge base systems — using Python, JavaScript (Tampermonkey), and C.',
          'Automated record keeping and operational processes across support workflows.',
          'Managed technical integrations for Google Fiber, ensuring high-performance connectivity.'
        ]
      },
      {
        title: 'Inbound Specialist',
        company: 'Schneider Electric',
        location: 'Athens, TX',
        period: 'December 2015 – March 2017',
        responsibilities: [
          'Managed inventory control, shipping, and data operations for a global supply chain network.',
          'Wrote SQL queries for inventory tracking, reporting, and data accuracy across supply chain systems.'
        ]
      }
    ])
    return { jobs }
  }
}
</script>
