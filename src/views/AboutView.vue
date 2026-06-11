<template>
  <div class="about container mx-auto px-6 py-16 max-w-3xl">
    <h1 class="font-display text-4xl text-zinc-100 mb-10" v-scroll-animation>About</h1>
    <div class="space-y-6 text-zinc-400 leading-relaxed" v-scroll-animation>
      <p>
        I'm an adaptable software engineer with seven-plus years of professional programming
        experience. My path has run through Amazon, Google Fiber, and Schneider Electric — and at
        every stop I found the manual process nobody questioned and replaced it with software:
        routing tools in Python and Java, QA databases, knowledge base systems, SQL reporting.
      </p>
      <p>
        Today I work at the front edge of AI engineering — designing MCP (Model Context Protocol)
        server integrations for enterprise platforms, building near-autonomous delivery pipelines,
        and engineering agentic workflows with Claude Code for top FAANG companies.
      </p>
      <p>
        I care about intelligent automation that holds up in regulated environments: compliance,
        audit traceability, and security are design inputs, not afterthoughts.
      </p>
    </div>
    <h2 class="font-display text-2xl text-zinc-100 mt-12 mb-6" v-scroll-animation>Focus Areas</h2>
    <ul class="grid sm:grid-cols-2 gap-3 text-zinc-300" v-scroll-animation>
      <li v-for="s in strengths" :key="s" class="bg-white/5 ring-1 ring-white/10 rounded-xl px-4 py-3 text-sm">{{ s }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AboutView',
  data() {
    return {
      strengths: [
        'AI-Driven Engineering & Agentic Workflows',
        'MCP Server Development',
        'Full-Stack Web Development',
        'Cloud-Native Architecture (AWS)',
        'Process Automation & Internal Tooling',
        'Regulated-Environment Delivery'
      ]
    }
  }
}
</script>
