---
layout: home
title: Welcome
---

<style>
  .center-links {
    text-align: center;
  }
  .post-item {
    display: flex;
    align-items: flex-start; /* Aligns items to the top of the flex container */
    margin-bottom: 2em; /* Spacing between posts */
    border-bottom: 1px solid #eee; /* Separator for posts */
    padding-bottom: 1.5em; /* Padding above the separator */
  }
  .post-image {
    flex-shrink: 0; /* Prevents the image from shrinking */
    width: 150px; /* Fixed width for the image */
    height: auto;
    margin-right: 1.5em; /* Space between image and text */
    border-radius: 4px; /* Slightly rounded corners for the image */
    object-fit: cover; /* Ensures the image covers the area without distortion */
  }
  .post-content {
    flex-grow: 1; /* Allows the content to take up remaining space */
  }
  .post-content h3 {
    margin-top: 0; /* Remove default top margin for heading */
    margin-bottom: 0.5em; /* Space below heading */
  }
  .post-content p {
    margin-bottom: 0.5em; /* Space below blurb */
  }
  .post-date {
    font-size: 0.9em;
    color: #555;
  }
</style>

Presented simply —

<div style="max-width: 700px; margin: 0 auto; padding-top: 1rem;">

  <img src="assets/images/logo.png" alt="headshot" style="width: 150px; float: right; margin-left: 20px; border-radius: 4px;">

  <p>
    I’m a data scientist and developer with a background in applied data science, business analytics, and ten years of military service.
    My work emphasizes system clarity, durable implementation, and straightforward design.
  </p>

  <p>
    I’m currently focused on cloud application development, model deployment, and generative systems.
  </p>

  <div class="center-links">
    <p>
      <a href="placeholder">Download Resume</a> ·
      <a href="https://github.com/MylesTym">GitHub</a> ·
      <a href="https://www.linkedin.com/in/myles-tym/">LinkedIn</a>
    </p>
  </div>

</div>

---

## Projects

{% for post in paginator.posts %}
  <div class="post-item">
    {% if post.image %}
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="post-image">
    {% endif %}
    <div class="post-content">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-date">{{ post.date | date: "%b %-d, %Y" }}</p>
      {% if post.blurb %}
        <p>{{ post.blurb }}</p>
      {% else %}
        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
    </div>
  </div>
{% endfor %}

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
