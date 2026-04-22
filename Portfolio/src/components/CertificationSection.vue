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
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
}

.cert-card {
  padding: 24px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.cert-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.platform {
  font-size: 12px;
  font-weight: 600;
  color: var(--accent);
  letter-spacing: 0.05em;
}

.year {
  font-size: 12px;
  color: var(--text-muted);
}

.cert-title {
  font-size: 16px;
  font-weight: 600;
  color: var(--text);
}

.cert-issuer {
  font-size: 14px;
  color: var(--text-muted);
}

.cert-link {
  margin-top: 6px;
  font-size: 13px;
  color: var(--accent);
  text-decoration: none;
}
.cert-request {
  margin-top: 6px;
  font-size: 13px;
  color: var(--text-muted);
  font-style: italic;
}
.cert-link:hover {
  text-decoration: underline;
}
</style>