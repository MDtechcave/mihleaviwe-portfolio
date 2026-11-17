
<template>
  <section class="about section">
    <div class="about-grid">

      <div class="about-text">
        <span class="section-label">About Me</span>

        <h2 class="title">
          Full-stack developer<br />
          <em>building for the web.</em>
        </h2>

        <p class="intro">
          I'm a Full-Stack Developer who enjoys turning ideas into
          functional web applications. I work across the frontend
          and backend, building user interfaces, developing APIs,
          and connecting applications to databases.
        </p>

        <p class="body">
          My core technologies include Python and FastAPI for backend
          development, Vue.js and Next.js for frontend development,
          and MySQL, Supabase, and Firebase for database management.
          I enjoy working across the full development process,
          solving problems, and continuously improving my skills
          by building practical applications.
        </p>
      </div>

      <div class="highlights">
        <div
          class="skill-card"
          v-for="item in skills"
          :key="item.title"
        >
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
  {
    icon: '⬡',
    title: 'Backend Development',
    desc: 'Python, FastAPI, REST APIs, authentication'
  },
  {
    icon: '⬡',
    title: 'Frontend Development',
    desc: 'Vue.js, Next.js, JavaScript, responsive interfaces'
  },
  {
    icon: '⬡',
    title: 'Databases',
    desc: 'MySQL, Supabase, PostgreSQL, Firebase'
  },
  {
    icon: '⬡',
    title: 'Full-Stack Development',
    desc: 'API integration, application logic, complete web applications'
  }
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
