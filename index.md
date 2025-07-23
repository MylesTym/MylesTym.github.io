---
layout: home
title: Welcome
---

Presented simply — Work and Projects

<div style="max-width: 700px; margin: 0 auto; padding-top: 1rem;">

  <img src="placeholder" alt="headshot" style="width: 150px; float: right; margin-left: 20px; border-radius: 4px;">

  <p>
    I’m a data scientist and developer with a background in applied data science, business analytics, and ten years of military service.
    My work emphasizes system clarity, durable implementation, and straightforward design.
  </p>

  <p>
    I’m currently focused on cloud application development, model deployment, and generative systems.
  </p>

  <p>
    <a href="placeholder">Download Resume</a> ·
    <a href="https://github.com/MylesTym">GitHub</a> ·
    <a href="placeholder">Contact</a>
  </p>

</div>

---

## Projects

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> — <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
