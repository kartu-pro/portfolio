---
layout: default
title: Home
---

# გამარჯობა, ჯაში ვარ 👋
### {{ site.description }}

{{ site.bio }}

---

## Georgian Related Projects

{% assign sorted_projects = site.projects | sort: "order" %}

<ul class="post-list" style="margin-left: 0; list-style: none;">
  {% for project in sorted_projects %}
    
    {% comment %} Define Category Colors {% endcomment %}
    {% case project.category %}
      {% when "logic" %}
        {% assign badge_color = "#e1f5fe" %}{% assign text_color = "#01579b" %}
      {% when "data" %}
        {% assign badge_color = "#e8f5e9" %}{% assign text_color = "#1b5e20" %}
      {% when "apps" %}
        {% assign badge_color = "#f3e5f5" %}{% assign text_color = "#4a148c" %}
      {% else %}
        {% assign badge_color = "#eeeeee" %}{% assign text_color = "#444444" %}
    {% endcase %}

    <li style="margin-bottom: 2.5rem; list-style: none;">
      <h3 style="margin-bottom: 5px;">
        <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
      </h3>

      <div style="margin-bottom: 8px; display: flex; align-items: center; gap: 10px;">
        <span style="background-color: {{ badge_color }}; color: {{ text_color }}; font-size: 0.7rem; font-weight: bold; padding: 2px 10px; border-radius: 4px; text-transform: uppercase; letter-spacing: 0.5px;">
          {{ project.category }}
        </span>

        {% if project.link_demo %}
          <a href="{{ project.link_demo }}" target="_blank" style="font-size: 0.8rem; font-weight: 600; color: #2a7ae2; text-decoration: none;">
            🚀 Live Demo
          </a>
        {% endif %}
      </div>

      <p style="margin-top: 0; color: #555; line-height: 1.5; font-size: 1.05rem;">
        {{ project.description }}
      </p>
    </li>
  {% endfor %}
</ul>

---

## Skills & Tools
* **Languages:** Python, JavaScript (ES6+), HTML, CSS, GoLang, SQL
* **Frameworks:** Pandas, Scikit-learn, CRFsuite, NLTK, Vue, Django, Flask, FastApi, Google Apps Script, Tailwind
* **Tools:** Vim, Git, bash, FFmpeg
