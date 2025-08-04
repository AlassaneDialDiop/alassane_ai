---
layout: default
title: Home
---

<div class="hero">
    <img src="{{ '/assets/alassane.webp' | relative_url }}" alt="Alassane" class="hero-image">
    <h1 class="hero-title">Welcome to Alassane.co</h1>
    <p class="hero-subtitle">Data Scientist | Machine Learning Expert | AI Consultant</p>
</div>

## Featured Work

<div class="card-grid">
    {% assign featured_projects = site.projects | sort: 'date' | reverse | limit: 3 %}
    {% for project in featured_projects %}
    <div class="card">
        <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
        <p>{{ project.subtitle }}</p>
        <div class="card-technologies">
            {% for tech in project.technologies limit:3 %}
            <span class="tech-tag">{{ tech }}</span>
            {% endfor %}
        </div>
    </div>
    {% endfor %}
</div>

<div class="view-all-projects">
    <a href="{{ '/projects/' | relative_url }}" class="button">View All Projects →</a>
</div>

## About Me

I'm Alassane Diop, a data scientist based in Montreal, passionate about leveraging AI and machine learning to solve real-world business challenges. Currently working at Browns Shoes and consulting for innovative startups, I specialize in building intelligent systems that drive business value.

[Learn more about me →]({{ '/about/' | relative_url }})