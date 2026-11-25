
<template>
  <section class="hero">
    <div class="hero-inner">

      <span class="section-label">Full-Stack Developer · Cape Town</span>

      <h2 class="title">
        Mihle<br />
        <em>Dudumashe</em>
      </h2>

      <p class="subtitle">
        Full-Stack Developer passionate about building functional
        web applications. I work across frontend and backend
        development, turning ideas into applications through
        clean interfaces, APIs and database integration.
      </p>

      <div class="hero-actions">
        <a href="mailto:mihleaviwe6@gmail.com" class="btn-primary">
          Get in Touch
        </a>

        <a href="/Mihle Dudumashe Resume.pdf" download class="btn-secondary">
          Download CV
        </a>
      </div>

      <div class="hero-skills">
        <div class="skill-pill"><span class="dot"></span>Python & FastAPI</div>
        <div class="skill-pill"><span class="dot"></span>Vue.js & Next.js</div>
        <div class="skill-pill"><span class="dot"></span>MySQL & PostgreSQL</div>
        <div class="skill-pill"><span class="dot"></span>Supabase & Firebase</div>
        <div class="skill-pill"><span class="dot"></span>REST APIs</div>
      </div>

    </div>

    <div class="hero-decoration" aria-hidden="true">
      <div class="deco-ring ring-1"></div>
      <div class="deco-ring ring-2"></div>
      <div class="deco-initials">MD</div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 88vh;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 48px;
  padding-top: 80px;
}

.hero-inner {
  max-width: 580px;
  flex: 1;
}

.title {
  font-size: clamp(52px, 7vw, 80px);
  margin: 0 0 24px;
  color: var(--text);
}

.title em {
  font-style: italic;
  color: var(--accent);
}

.subtitle {
  font-size: 17px;
  line-height: 1.75;
  color: var(--text-muted);
  margin-bottom: 36px;
  max-width: 480px;
}

.hero-actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-bottom: 40px;
}

.btn-primary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 24px;
  background: var(--accent);
  color: #0d1117;
  border-radius: var(--radius-sm);
  font-size: 14px;
  font-weight: 600;
  font-family: var(--font-body);
  letter-spacing: 0.01em;
  transition: opacity 0.2s ease;
}

.btn-primary:hover {
  opacity: 0.85;
  color: #0d1117;
}

.btn-secondary {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 12px 24px;
  border-radius: var(--radius-sm);
  font-size: 14px;
  font-weight: 500;
  font-family: var(--font-body);
  color: var(--text-muted);
  border: 1px solid var(--border);
  background: transparent;
  transition: border-color 0.2s ease, color 0.2s ease;
}

.btn-secondary:hover {
  border-color: var(--accent);
  color: var(--accent);
  opacity: 1;
}

.hero-skills {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.skill-pill {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  padding: 6px 12px;
  border-radius: var(--radius-sm);
  font-size: 12px;
  font-weight: 500;
  color: var(--text-muted);
  background: var(--bg-soft);
  border: 1px solid var(--border);
}

.dot {
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background: var(--accent);
  display: inline-block;
  flex-shrink: 0;
}

/* Decoration */
.hero-decoration {
  flex-shrink: 0;
  width: 260px;
  height: 260px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.deco-ring {
  position: absolute;
  border-radius: 50%;
}

.ring-1 {
  width: 260px;
  height: 260px;
  border: 1px solid var(--accent-mid);
  opacity: 0.5;
  animation: spin 20s linear infinite;
}

.ring-2 {
  width: 200px;
  height: 200px;
  border: 1px dashed var(--border);
  animation: spin 28s linear infinite reverse;
}

.deco-initials {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  background: var(--bg-soft);
  border: 1px solid var(--accent-mid);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-size: 38px;
  color: var(--accent);
  letter-spacing: -0.02em;
  z-index: 1;
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

@media (max-width: 820px) {
  .hero {
    flex-direction: column;
    align-items: flex-start;
    min-height: unset;
    padding-top: 60px;
  }

  .hero-decoration {
    display: none;
  }
}

@media (max-width: 480px) {
  .title {
    font-size: 46px;
  }
}
</style>
