<template>
  <section class="certifications section">

    <div class="section-header">
      <span class="section-label">Certifications</span>
      <h2 class="title">Credentials</h2>
      <p class="subtitle">
        A collection of certifications and courses I completed to build technical skills.
      </p>
    </div>

    <div class="grid">
      <div class="card cert-card" v-for="cert in certifications" :key="cert.title">

        <div class="cert-top">
          <span class="platform">{{ cert.platform }}</span>
          <span class="year">{{ cert.year }}</span>
        </div>

        <h2 class="cert-title">{{ cert.title }}</h2>
        <p class="cert-issuer">{{ cert.issuer }}</p>

        <a v-if="cert.link" :href="cert.link" target="_blank" class="cert-link">
        View Certificate
        </a>

        <span v-else class="cert-request">
        Available upon request
        </span>
      </div>
    </div>

  </section>
</template>

<script setup>
const certifications = [
  {
    title: "Introduction to Cybersecurity",
    issuer: "Credly",
    platform: "Cisco Networking Academy",
    year: "2026",
    link: "https://www.credly.com/badges/2ec9ea7f-958b-4a3f-a5da-e0612ef936b4/public_url"
  },
  {
    title: "Introduction to Data Science",
    issuer: "Credly",
    platform: "Cisco Networking Academy",
    year: "2026",
    link: "https://www.credly.com/badges/b432a16f-dff2-4edd-adc8-93a3927ab9e7/public_url"
  },
    {
    title: "Full Stack Development",
    issuer: "Life Choices Academy",
    platform: "Life Choices Academy",
    year: "2026",
    link: ""
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
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
}

.cert-card {
  padding: 28px;
  display: flex;
  flex-direction: column;
  gap: 14px;
}

/* Match project card top layout */
.cert-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.platform {
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.1em;
  color: var(--accent);
}

.year {
  font-size: 12px;
  color: var(--text-muted);
}

/* Match project title */
.cert-title {
  font-size: 18px;
  font-weight: 600;
  color: var(--text);
}

/* Match project description style */
.cert-issuer {
  font-size: 14px;
  line-height: 1.6;
  color: var(--text-muted);
}

/* Link styles aligned with project icons/text */
.cert-link,
.cert-request {
  margin-top: auto;
  font-size: 13px;
}

.cert-link {
  color: var(--accent);
  text-decoration: none;
  transition: opacity 0.2s ease;
}

.cert-link:hover {
  opacity: 0.7;
}

.cert-request {
  color: var(--text-muted);
  font-style: italic;
}
</style>