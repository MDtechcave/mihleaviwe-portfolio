<template>
  <section class="certifications section">

    <div class="section-header">
      <span class="section-label">Certifications</span>
      <h2 class="title">Credentials</h2>
      <p class="subtitle">Certifications completed to build and validate technical skills.</p>
    </div>

    <div class="grid">
      <div class="cert-card" v-for="cert in certifications" :key="cert.title">

        <div class="cert-top">
          <span class="platform">{{ cert.platform }}</span>
          <span class="year">{{ cert.year }}</span>
        </div>

        <h3 class="cert-title">{{ cert.title }}</h3>
        <p class="cert-issuer">{{ cert.issuer }}</p>

        <a v-if="cert.link" :href="cert.link" target="_blank" class="cert-link">
          View Certificate →
        </a>
        <span v-else class="cert-request">Available upon request</span>

      </div>
    </div>

  </section>
</template>

<script setup>
const certifications = [
  {
    title:    'Introduction to Cybersecurity',
    issuer:   'Credly',
    platform: 'Cisco Networking Academy',
    year:     '2026',
    link:     'https://www.credly.com/badges/2ec9ea7f-958b-4a3f-a5da-e0612ef936b4/public_url'
  },
  {
    title:    'Introduction to Data Science',
    issuer:   'Credly',
    platform: 'Cisco Networking Academy',
    year:     '2026',
    link:     'https://www.credly.com/badges/b432a16f-dff2-4edd-adc8-93a3927ab9e7/public_url'
  },
  {
    title:    'Full Stack Development',
    issuer:   'Life Choices Academy',
    platform: 'Life Choices Academy',
    year:     '2026',
    link:     ''
  },
]
</script>

<style scoped>
.title {
  font-size: clamp(30px, 4vw, 46px);
  margin-bottom: 12px;
  line-height: 1.15;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1px;
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  overflow: hidden;
  background: var(--border);
}

.cert-card {
  padding: 28px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  background: var(--bg-card);
  transition: background 0.2s ease;
}

.cert-card:hover {
  background: var(--bg-soft);
}

.cert-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.platform {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.08em;
  color: var(--accent);
  text-transform: uppercase;
}

.year {
  font-size: 12px;
  color: var(--text-light);
}

.cert-title {
  font-size: 15px;
  font-weight: 600;
  color: var(--text);
}

.cert-issuer {
  font-size: 13px;
  color: var(--text-muted);
  flex: 1;
}

.cert-link {
  font-size: 12px;
  color: var(--accent);
  text-decoration: none;
  margin-top: auto;
  transition: opacity 0.2s ease;
}

.cert-link:hover {
  opacity: 0.7;
}

.cert-request {
  font-size: 12px;
  color: var(--text-light);
  font-style: italic;
  margin-top: auto;
}
</style>