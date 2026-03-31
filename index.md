---
layout: default
title: Home
---

# გამარჯობა, ჯაში ვარ 👋
### [ {{ site.description }} ]

{{ site.bio }}

---

## Georgian Related Projects

{% assign sorted_projects = site.projects | sort: "order" %}
{% for project in sorted_projects %}
### [{{ project.title }}]({{ site.baseurl }}{{ project.url }})
{{ project.description }}
{% endfor %}

---

## Skills & Tools
* **Languages:** Python, JavaScript (ES6+), HTML, CSS, GoLang, SQL
* **Frameworks:** Pandas, Scikit-learn, NLTK, Vue, Django, Flask, FastApi, Google Apps Script, Tailwind
* **Tools:** Vim, Git, bash
