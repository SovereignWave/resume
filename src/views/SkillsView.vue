<template>
  <div class="skills container mx-auto px-6 py-16 max-w-4xl">
    <h1 class="font-display text-4xl text-zinc-100 mb-12" v-scroll-animation>Technical Skills</h1>
    <div class="grid md:grid-cols-2 gap-6">
      <div v-for="(group, index) in skillGroups" :key="index"
           class="bg-white/5 backdrop-blur rounded-2xl ring-1 ring-white/10 p-6"
           v-scroll-animation>
        <h2 class="font-display text-xl text-gold-300 mb-4">{{ group.category }}</h2>
        <div class="flex flex-wrap gap-2">
          <span v-for="skill in group.items" :key="skill"
                class="text-xs text-zinc-300 bg-white/5 ring-1 ring-white/10 rounded-full px-3 py-1.5">
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SkillsView',
  data() {
    return {
      skillGroups: [
        {
          category: 'AI & Automation',
          items: ['Prompt Engineering', 'Agentic Workflows', 'Claude Code', 'MCP Server Development', 'AI-Assisted Code Generation', 'AI Model Evaluation']
        },
        {
          category: 'Languages',
          items: ['JavaScript', 'Python', 'Java', 'SQL', 'C', 'HTML/CSS']
        },
        {
          category: 'Web & Frameworks',
          items: ['React', 'Vue.js', 'Node.js', 'REST APIs', 'WordPress', 'Tailwind CSS']
        },
        {
          category: 'Cloud & DevOps',
          items: ['AWS (EC2, Lambda, S3)', 'CI/CD Pipelines', 'GitHub Actions', 'Serverless Patterns', 'Git']
        },
        {
          category: 'Integrations',
          items: ['MCP Protocol', 'OAuth 2.0', 'OpenID Connect', 'QuickBooks API', 'Bloomberg API', 'SOAP']
        },
        {
          category: 'Data & Compliance',
          items: ['PostgreSQL', 'Tableau', 'Data Pipelines', 'HIPAA Awareness', 'SOC 2 Concepts', 'Audit Traceability']
        }
      ]
    }
  }
}
</script>
