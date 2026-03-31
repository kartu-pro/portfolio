---
layout: default
title: Home
---

# გამარჯობა, ჯაში ვარ 👋
### [{{ site.description }} ]

{{ site.bio }}

---

## Georgian Related Projects

{% for project in site.projects %}
### [{{ project.title }}]({{ site.baseurl }}{{ project.url }})
{{ project.description }}
{% endfor %}

---

## Skills & Tools
* **Languages:** Python, JavaScript (ES6+), HTML, CSS, GoLang, SQL
* **Frameworks:** Pandas, Scikit-learn, NLTK, Vue, Django, Flask, FastApi, Google Apps Script, Tailwind
* **Tools:** Vim, Git, Linux CLI
