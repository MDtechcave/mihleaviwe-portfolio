<template>
  <section class="about section">
    <div class="about-grid">
 
      <!-- Left: text -->
      <div class="about-text">
        <span class="section-label">About Me</span>
        <h2 class="title">
          Developer with a<br />
          <em>systems mindset</em>
        </h2>
        <p class="intro">
          I'm a Full Stack Developer focused on building clean, responsive, and scalable
          web applications using modern technologies.
        </p>
        <p class="body">
          I work mainly with Vue, Node.js, Python, and SQL databases. I enjoy solving
          real-world problems through code and continuously improving both my technical
          and system-thinking skills. I'm also actively expanding into cybersecurity and
          SOC operations.
        </p>
      </div>
 
      <!-- Right: skill cards -->
      <div class="highlights">
        <div class="card skill-card" v-for="item in skills" :key="item.title">
          <div class="card-icon">{{ item.icon }}</div>
          <div>
            <h2 class="card-title">{{ item.title }}</h2>
            <p class="card-desc">{{ item.desc }}</p>
          </div>
        </div>
      </div>
 
    </div>
  </section>
</template>
 
<script setup>
const skills = [
  { icon: '⬡', title: 'Frontend',         desc: 'Vue, UI design, responsive layouts' },
  { icon: '⬡', title: 'Backend',          desc: 'Node.js, REST APIs, authentication' },
  { icon: '⬡', title: 'Databases',        desc: 'SQL, data modeling, optimization' },
  { icon: '⬡', title: 'Security',         desc: 'SOC concepts & system defense' },
]
</script>
 
<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: start;
}
 
/* Left text */
.about-text .title {
  font-size: clamp(32px, 4vw, 46px);
  margin-bottom: 24px;
  line-height: 1.15;
}
 
.about-text .title em {
  font-style: italic;
  color: var(--accent);
}
 
.intro {
  font-size: 17px;
  line-height: 1.75;
  color: var(--text-muted);
  margin-bottom: 16px;
}
 
.body {
  font-size: 15px;
  line-height: 1.8;
  color: var(--text-light);
}
 
/* Right cards */
.highlights {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px;
}
 
.skill-card {
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
 
.card-icon {
  font-size: 20px;
  color: var(--accent);
  line-height: 1;
}
 
.card-title {
  font-size: 14px;
  font-weight: 600;
  color: var(--text);
  margin-bottom: 4px;
}
 
.card-desc {
  font-size: 13px;
  color: var(--text-light);
  line-height: 1.55;
}
 
/* Responsive */
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