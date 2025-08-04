---
layout: page
title: Projects
permalink: /projects/
---

## My Work

Here's a selection of data science and AI projects I've worked on, showcasing my expertise in machine learning, NLP, recommendation systems, and data visualization.

<div class="projects-grid">
{% for project in site.projects %}
  <div class="project-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    <p class="project-subtitle">{{ project.subtitle }}</p>
    <div class="project-meta">
      <span class="project-date">{{ project.date | date: "%B %Y" }}</span>
    </div>
    <div class="project-technologies">
      {% for tech in project.technologies limit:4 %}
        <span class="tech-tag">{{ tech }}</span>
      {% endfor %}
      {% if project.technologies.size > 4 %}
        <span class="tech-tag">+{{ project.technologies.size | minus: 4 }} more</span>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.project-card {
  background: #f8f9fa;
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid #e9ecef;
  transition: transform 0.2s, box-shadow 0.2s;
}

.project-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.project-card h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

.project-card h3 a {
  color: #333;
  text-decoration: none;
}

.project-card h3 a:hover {
  color: #0066cc;
}

.project-subtitle {
  color: #666;
  font-size: 0.95rem;
  margin-bottom: 1rem;
  line-height: 1.4;
}

.project-meta {
  margin-bottom: 1rem;
}

.project-date {
  color: #888;
  font-size: 0.9rem;
}

.project-technologies {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tech-tag {
  background: #e9ecef;
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.85rem;
  color: #495057;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>