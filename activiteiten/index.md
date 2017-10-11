---
layout: page
title: Uitdagende activiteiten
menu_index: 4
parent: index
published: true
---

Op deze pagina vind je ideeën voor uitdagende activiteiten voor slimme peuters. Klik op de titel voor de beschrijving van de activiteit.

{% assign sorted_pages = site.pages | sort:"menu_index" %}
{% for my_page in sorted_pages %}
  {%- if my_page.menu_index and my_page.parent and my_page.parent == "activiteiten" -%}{{ "" }}
## [{{ my_page.title }}]({{ my_page.url | prepend: site.baseurl }})
    {%- assign sorted_tags = my_page.tags | sort %}
    {%- for tag in sorted_tags -%}{{ "" }}
{{ tag }}
{% if forloop.last == false %} | {% endif %}
    {%- endfor -%}
  {%- endif -%}
{% endfor %}
