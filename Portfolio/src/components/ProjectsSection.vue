<template>
  <section class="projects section">

    <div class="section-header">
      <span class="section-label">Projects</span>
      <h2 class="title">Selected Work</h2>
      <p class="subtitle">A sample of projects built across the full stack.</p>
    </div>

    <div class="grid">
      <div class="card project-card" v-for="(project, i) in projects" :key="project.title">
        <div class="card-top">
          <span class="project-number">0{{ i + 1 }}</span>
          <div class="card-links">
            <a v-if="project.github" :href="project.github" target="_blank" class="icon-link" aria-label="GitHub">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.02 10.02 0 0 0 22 12.017C22 6.484 17.522 2 12 2Z"/></svg>
            </a>
          </div>
        </div>

        <h1 class="project-title">{{ project.title }}</h1>
        <p class="project-desc">{{ project.desc }}</p>

        <div class="tags">
          <span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span>
        </div>
      </div>
    </div>

  </section>
</template>

<script setup>
const projects = [
  {
    title:  'Imvelaphi Gallery',
    desc:   'Cultural gallery showcasing Xhosa heritage through an interactive, responsive web experience designed to educate and engage.',
    tags:   ['HTML', 'CSS', 'JavaScript'],
    github: 'https://github.com/MDtechcave/My-Gallery',
    live: 'https://your-live-site.com'
  },
  {
    title:  'Healthy Habits',
    desc:   'E-commerce meal subscription platform with user accounts, subscription management, and loyalty-based discount logic.',
    tags:   ['Vue', 'MySQL', 'Node.js'],
    github: 'https://github.com/MDtechcave/Frontend',
  },
  {
    title:  'StaffSync',
    desc:   'HR management system for employee records, payroll processing, and automated payslip generation.',
    tags:   ['Vue', 'Node.js'],
    github: 'https://github.com/MDtechcave/Moderntech_center',
  },
]
</script>
<style scoped>
.title {
  font-size: clamp(32px, 4vw, 48px);
  margin-bottom: 18px;
  line-height: 1.15;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
}

.project-card {
  padding: 24px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.card-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.project-number {
  font-size: 12px;
  font-weight: 600;
  color: var(--accent);
  letter-spacing: 0.05em;
}

.icon-link {
  width: 28px;
  height: 28px;
  border-radius: 6px;
  background: transparent;
  border: none;
  color: var(--text-muted);
}

.icon-link:hover {
  color: var(--accent);
}

/* Match cert title size */
.project-title {
  font-size: 16px;
  font-weight: 600;
  color: var(--text);
}

/* Match cert text */
.project-desc {
  font-size: 14px;
  color: var(--text-muted);
  line-height: 1.6;
}

/* Tags (simplified) */
.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-top: 6px;
}

.tag {
  font-size: 11px;
  padding: 4px 8px;
  border-radius: 6px;
  background: var(--bg-soft);
  color: var(--text-muted);
  border: 1px solid var(--border);
}
</style>
