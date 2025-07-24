---
layout: home
title: Welcome
---

Presented simply —

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
  {% for post in paginator.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> — <small>{{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
  <nav class="pagination" role="navigation">
    {% if paginator.previous_page %}
      {# If on page 2 or higher, "Previous" links back to the root (for page 1) or a specific /pageX/ #}
      {% assign prev_url = paginator.previous_page_path %}
      {% if paginator.previous_page == 1 %}
        {% assign prev_url = "/" %} {# Special case: previous from page 2 goes to root #}
      {% endif %}
      <a href="{{ prev_url | relative_url }}" class="previous">Previous</a>
    {% endif %}

    {% for page_number in (1..paginator.total_pages) %}
      {% if page_number == paginator.page %}
        <span class="page current">{{ page_number }}</span>
      {% else %}
        {# Determine the correct URL for the page number #}
        {% assign page_url = paginator.paginate_path | replace: ':num', page_number %}
        {% if page_number == 1 %}
          {% assign page_url = "/" %} {# Special case: page 1 link points to the root #}
        {% endif %}
        <a href="{{ page_url | relative_url }}" class="page">{{ page_number }}</a>
      {% endif %}
    {% endfor %}

    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | relative_url }}" class="next">Next</a>
    {% endif %}
  </nav>
{% endif %}
