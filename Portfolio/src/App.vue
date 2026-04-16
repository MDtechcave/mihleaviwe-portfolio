<template>
  <div class="app-wrapper">
    <main class="page">
      <HeroSection />
      <AboutSection />
      <ProjectsSection />
      <CertificationSection />
      <ContactSection />

    </main>
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import CertificationSection from './components/CertificationSection.vue'
import ContactSection from './components/ContactSection.vue'
</script>

<style>
.app-wrapper {
  min-height: 100vh;
  background: var(--bg);
  color: var(--text);
}

.page {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 32px;
}

@media (max-width: 768px) {
  .page {
    padding: 0 20px;
  }
}
</style>