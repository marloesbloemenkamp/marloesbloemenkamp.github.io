---
layout: default
---

{% assign sorted_pages = site.pages | sort:"menu_index" %}
{% for my_page in sorted_pages %}
  {% if my_page.menu_index and my_page.parent == "index" %}
  [{{ my_page.title }}]({{ my_page.url | prepend: site.baseurl }})
  {% endif %}
{% endfor %}
