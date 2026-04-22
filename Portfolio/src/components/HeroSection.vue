<template>
  <section class="hero">
    <div class="hero-inner">

      <span class="section-label">Full Stack Developer · Based in Cape Town</span>

      <h2 class="title">
        Mihle<br />
        <em>Dudumashe</em>
      </h2>

      <p class="subtitle">
        Building clean, scalable web applications with Vue, Node &amp; Python.
        Passionate about systems thinking, security, and performance-driven design.
      </p>

      <div class="hero-actions">
        <a href="mailto:mihleaviwe6@gmail.com" class="btn-primary">Get in Touch</a>
      </div>

      <div class="hero-skills">
        <div class="skill-pill">
          <span class="dot"></span>Frontend
        </div>
        <div class="skill-pill">
          <span class="dot"></span>Backend
        </div>
        <div class="skill-pill">
          <span class="dot"></span>Databases
        </div>
        <div class="skill-pill">
          <span class="dot"></span>Security
        </div>
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

/* Left content */
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

/* CTA buttons */
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
  padding: 13px 26px;
  background: var(--accent);
  color: #fff;
  border-radius: 999px;
  font-size: 14px;
  font-weight: 500;
  font-family: var(--font-body);
  letter-spacing: 0.01em;
  transition: background 0.2s ease, transform 0.2s ease, box-shadow 0.2s ease;
  box-shadow: 0 2px 12px rgba(43, 92, 230, 0.25);
}

.btn-primary:hover {
  background: #1d45cc;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(43, 92, 230, 0.35);
  opacity: 1;
}

.btn-secondary {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 13px 22px;
  border-radius: 999px;
  font-size: 14px;
  font-weight: 500;
  font-family: var(--font-body);
  color: var(--text);
  border: 1.5px solid var(--border);
  background: var(--bg-card);
  transition: border-color 0.2s ease, transform 0.2s ease, box-shadow 0.2s ease;
  box-shadow: var(--shadow-sm);
}

.btn-secondary:hover {
  border-color: var(--accent-mid);
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
  opacity: 1;
  color: var(--text);
}

/* Skills pills */
.hero-skills {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.skill-pill {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  padding: 7px 14px;
  border-radius: 999px;
  font-size: 12.5px;
  font-weight: 500;
  color: var(--text-muted);
  background: var(--bg-soft);
  border: 1px solid var(--border);
}

.dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--accent);
  display: inline-block;
  flex-shrink: 0;
}

/* Right decoration */
.hero-decoration {
  flex-shrink: 0;
  width: 280px;
  height: 280px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.deco-ring {
  position: absolute;
  border-radius: 50%;
  border: 1.5px solid var(--border);
}

.ring-1 {
  width: 280px;
  height: 280px;
  border-color: var(--accent-mid);
  opacity: 0.4;
  animation: spin 18s linear infinite;
}

.ring-2 {
  width: 220px;
  height: 220px;
  border-color: var(--border);
  border-style: dashed;
  animation: spin 24s linear infinite reverse;
}

.deco-initials {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  background: var(--accent-soft);
  border: 1.5px solid var(--accent-mid);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-size: 42px;
  color: var(--accent);
  letter-spacing: -0.02em;
  z-index: 1;
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to   { transform: rotate(360deg); }
}

/* Responsive */
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