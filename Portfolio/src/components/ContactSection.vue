<template>
  <section class="contact section">

    <div class="contact-inner">

      <div class="contact-text">
        <span class="section-label">Contact</span>
        <h2 class="title">Let's work<br /><em>together</em></h2>
        <p class="subtitle">
          Open to full-time roles, freelance projects, and internship opportunities.
          Feel free to reach out - I'd love to connect.
        </p>
      </div>

      <div class="contact-links">

        <a href="mailto:mihleaviwe6@gmail.com" class="contact-card">
          <div class="contact-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/>
            </svg>
          </div>
          <div class="contact-info">
            <span class="contact-type">Email</span>
            <span class="contact-value">mihleaviwe6@gmail.com</span>
          </div>
          <svg class="arrow" width="16" height="16" viewBox="0 0 14 14" fill="none"><path d="M2 12L12 2M12 2H5M12 2V9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>

        <a href="https://github.com/MDtechcave" target="_blank" class="contact-card">
          <div class="contact-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.59 9.59 0 0 1 2.504.337c1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.02 10.02 0 0 0 22 12.017C22 6.484 17.522 2 12 2Z"/></svg>
          </div>
          <div class="contact-info">
            <span class="contact-type">GitHub</span>
            <span class="contact-value">MDtechcave</span>
          </div>
          <svg class="arrow" width="16" height="16" viewBox="0 0 14 14" fill="none"><path d="M2 12L12 2M12 2H5M12 2V9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>

        <a href="https://www.linkedin.com/in/mihle-dudumashe-53642a3b1" target="_blank" class="contact-card">
          <div class="contact-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
          </div>
          <div class="contact-info">
            <span class="contact-type">LinkedIn</span>
            <span class="contact-value">Mihle Dudumashe</span>
          </div>
          <svg class="arrow" width="16" height="16" viewBox="0 0 14 14" fill="none"><path d="M2 12L12 2M12 2H5M12 2V9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>

      </div>

    </div>

  
    <div class="footer">
      <p>© {{ new Date().getFullYear() }} Mihle Aviwe Dudumashe · Developer</p>
    </div>

  </section>
</template>

<style scoped>
.contact-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: start;
  margin-bottom: 64px;
}

/* Text side */
.title {
  font-size: clamp(32px, 4vw, 48px);
  margin-bottom: 18px;
  line-height: 1.15;
}

.title em {
  font-style: italic;
  color: var(--accent);
}

.subtitle {
  font-size: 16px;
  line-height: 1.75;
  color: var(--text-muted);
  max-width: 360px;
}

/* Contact link cards */
.contact-links {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.contact-card {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 18px 20px;
  border-radius: var(--radius-md);
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  box-shadow: var(--shadow-sm);
  color: var(--text);
  text-decoration: none;
  transition: transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease;
}

.contact-card:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-md);
  border-color: var(--accent-mid);
  opacity: 1;
  color: var(--text);
}

.contact-icon {
  width: 42px;
  height: 42px;
  border-radius: 10px;
  background: var(--accent-soft);
  border: 1px solid var(--accent-mid);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--accent);
  flex-shrink: 0;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 2px;
  flex: 1;
}

.contact-type {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--text-light);
}

.contact-value {
  font-size: 14px;
  font-weight: 500;
  color: var(--text);
}

.arrow {
  color: var(--text-light);
  flex-shrink: 0;
  transition: color 0.2s ease, transform 0.2s ease;
}

.contact-card:hover .arrow {
  color: var(--accent);
  transform: translate(2px, -2px);
}

/* Footer */
.footer {
  border-top: 1px solid var(--border);
  padding-top: 28px;
  text-align: center;
}

.footer p {
  font-size: 13px;
  color: var(--text-light);
}

/* Responsive */
@media (max-width: 820px) {
  .contact-inner {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .subtitle {
    max-width: 100%;
  }
}
</style>