
<template>
  <section id="projects" class="projects-section">
    <div class="section-container">

      <div class="section-heading">
        <span class="section-label">MY WORK</span>
        <h2>Projects I've built.</h2>
        <p>
          Applications and systems I've built to solve practical problems
          and explore different technologies.
        </p>
      </div>

      <div class="projects-grid">
        <article
          v-for="(project, index) in projects"
          :key="project.title"
          class="project-card"
        >
          <div class="project-top">
            <span class="project-number">
              {{ String(index + 1).padStart(2, '0') }}
            </span>

            <span class="project-type">
              {{ project.type }}
            </span>
          </div>

          <div class="project-content">
            <h3>{{ project.title }}</h3>

            <p class="project-description">
              {{ project.description }}
            </p>

            <div class="project-tags">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="project-tag"
              >
                {{ tag }}
              </span>
            </div>
          </div>

          <div class="project-links">
            <a
              v-if="project.github"
              :href="project.github"
              target="_blank"
              rel="noopener noreferrer"
              class="project-link"
            >
              GitHub
              <span>↗</span>
            </a>

            <a
              v-if="project.live"
              :href="project.live"
              target="_blank"
              rel="noopener noreferrer"
              class="project-link"
            >
              Live Demo
              <span>↗</span>
            </a>

            <span
              v-if="!project.github && !project.live"
              class="project-coming-soon"
            >
              Links coming soon
            </span>
          </div>
        </article>
      </div>

    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: "StaffSync",
    type: "Full-Stack Web Application",
    description:
      "An HR management application designed to simplify employee management. It includes role-based access, employee records, leave management, payroll functionality and payslip management.",
    tags: [
      "Python",
      "FastAPI",
      "Vue.js",
      "Supabase",
      "PostgreSQL"
    ],
    github: "https://github.com/MDtechcave/Moderntech_center",
    live: "https://moderntech-center.vercel.app/"
  },

  

{
  title: "Kopano Industrial Supply",
  type: "Full-Stack Web Application · Assessment Project",
  description:
    "A B2B catalogue and quotation management platform where customers can browse industrial products and submit requests for quotations. Features role-based access for clients, sales staff and administrators, an admin team management dashboard, a REST API and automated backend tests.",
  tags: [
    "Python",
    "FastAPI",
    "React",
    "SQLite",
    "REST APIs",
    "Pytest",
    "Role-Based Authentication"
  ],
  github: "https://github.com/MDtechcave/kopano.git",
  live: "kopano-tan.vercel.app",
  demoAccounts: [

    {
      role: "Sales",
      email: "tumelo@example.com",
      password: "tumelokafi7784"
    },
    {
      role: "Admin",
      email: "admin@example.com",
      password: "lewismikey@kopano"
    }
  ]
},


  {
    title: "Lungisani",
    type: "Mobile Application · Personal Project",
    description:
      "A civic reporting application that allows Cape Town residents to report municipal issues such as potholes, water problems, sewage and uncollected waste. Residents can submit reports with photos, view community reports and upvote existing issues to make recurring problems more visible.",
    tags: [
      "Flutter",
      "Dart",
      "Supabase",
      "Riverpod",
      "PostgreSQL"
    ],
    github: "",
    live: ""
  }
];
</script>

<style scoped>
.projects-section {
  padding: 100px 24px;
  background: var(--bg-primary, #ffffff);
}

.section-container {
  max-width: 1150px;
  margin: 0 auto;
}

.section-heading {
  max-width: 650px;
  margin-bottom: 55px;
}

.section-label {
  display: inline-block;
  margin-bottom: 15px;
  color: var(--accent-color, #64748b);
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 2px;
}

.section-heading h2 {
  margin: 0 0 15px;
  color: var(--text-primary, #172033);
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 750;
  letter-spacing: -1.5px;
}

.section-heading p {
  margin: 0;
  color: var(--text-secondary, #64748b);
  font-size: 1rem;
  line-height: 1.8;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 24px;
}

.project-card {
  display: flex;
  flex-direction: column;
  min-height: 340px;
  padding: 30px;
  border: 1px solid var(--border-color, #e5e7eb);
  border-radius: 18px;
  background: var(--card-bg, #ffffff);
  transition:
    transform 0.25s ease,
    border-color 0.25s ease,
    box-shadow 0.25s ease;
}

.project-card:hover {
  transform: translateY(-5px);
  border-color: var(--accent-color, #64748b);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.06);
}

.project-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  margin-bottom: 30px;
}

.project-number {
  color: var(--accent-color, #64748b);
  font-size: 0.85rem;
  font-weight: 700;
}

.project-type {
  color: var(--text-secondary, #64748b);
  font-size: 0.72rem;
  text-align: right;
}

.project-content {
  flex: 1;
}

.project-content h3 {
  margin: 0 0 14px;
  color: var(--text-primary, #172033);
  font-size: 1.4rem;
  font-weight: 700;
}

.project-description {
  margin: 0;
  color: var(--text-secondary, #64748b);
  font-size: 0.92rem;
  line-height: 1.8;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 24px;
}

.project-tag {
  padding: 7px 11px;
  border: 1px solid var(--border-color, #e5e7eb);
  border-radius: 6px;
  color: var(--text-secondary, #64748b);
  font-size: 0.75rem;
  font-weight: 500;
}

.project-links {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin-top: 28px;
  padding-top: 20px;
  border-top: 1px solid var(--border-color, #e5e7eb);
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  color: var(--text-primary, #172033);
  font-size: 0.85rem;
  font-weight: 650;
  text-decoration: none;
  transition: color 0.2s ease;
}

.project-link:hover {
  color: var(--accent-color, #64748b);
}

.project-link span {
  font-size: 1rem;
}

@media (max-width: 700px) {
  .projects-section {
    padding: 75px 18px;
  }

  .projects-grid {
    grid-template-columns: 1fr;
  }

  .project-card {
    min-height: auto;
    padding: 24px;
  }

  .project-top {
    align-items: flex-start;
    flex-direction: column;
  }

  .project-type {
    text-align: left;
  }
}
</style>
