<template>
  <section class="about section">
    <div class="about-grid">

      <div class="about-text">
        <span class="section-label">About Me</span>
        <h2 class="title">
          Full-stack dev with a<br />
          <em>backend-first mindset</em>
        </h2>
        <p class="intro">
          I focus on what happens on the server, API design, database logic,
          authentication, and system architecture. The frontend comes along for the ride.
        </p>
        <p class="body">
          My main stack is Node.js, Python/FastAPI, Vue, and SQL databases including
          MySQL and Supabase/PostgreSQL. I've built production-level systems with
          role-based access control, SQL triggers, payroll logic, and REST APIs.
        </p>
      </div>

      <div class="highlights">
        <div class="skill-card" v-for="item in skills" :key="item.title">
          <div class="card-icon">{{ item.icon }}</div>
          <div>
            <h3 class="card-title">{{ item.title }}</h3>
            <p class="card-desc">{{ item.desc }}</p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const skills = [
  { icon: '⬡', title: 'Backend',   desc: 'Node.js, Python, FastAPI, REST APIs, auth' },
  { icon: '⬡', title: 'Databases', desc: 'MySQL, PostgreSQL, Supabase, SQL triggers' },
  { icon: '⬡', title: 'Frontend',  desc: 'Vue, React, responsive UI, clean layouts' },
  { icon: '⬡', title: 'DevOps',    desc: 'Git, Vercel, Render, Netlify, deployment' },
]
</script>

<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: start;
}

.about-text .title {
  font-size: clamp(30px, 4vw, 44px);
  margin-bottom: 24px;
  line-height: 1.15;
}

.about-text .title em {
  font-style: italic;
  color: var(--accent);
}

.intro {
  font-size: 16px;
  line-height: 1.75;
  color: var(--text-muted);
  margin-bottom: 16px;
}

.body {
  font-size: 14px;
  line-height: 1.8;
  color: var(--text-light);
}

.highlights {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2px;
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  overflow: hidden;
}

.skill-card {
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  background: var(--bg-card);
  border-right: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  transition: background 0.2s ease;
}

.skill-card:hover {
  background: var(--bg-soft);
}

.card-icon {
  font-size: 18px;
  color: var(--accent);
  line-height: 1;
}

.card-title {
  font-size: 13px;
  font-weight: 600;
  color: var(--text);
  margin-bottom: 4px;
}

.card-desc {
  font-size: 12px;
  color: var(--text-muted);
  line-height: 1.55;
}

@media (max-width: 820px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}

@media (max-width: 480px) {
  .highlights {
    grid-template-columns: 1fr;
  }
}
</style>