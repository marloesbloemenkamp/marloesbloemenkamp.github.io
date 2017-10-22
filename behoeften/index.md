---
layout: page
title: Wat hebben slimme peuters nodig?
menu_index: 2
parent: index
---

<img src="/images/peers.png" class="centered" />

De volgende aspecten zijn belangrijk voor peuters met een ontwikkelingsvoorsprong:

{% assign sorted_pages = site.pages | sort:"menu_index" %}
{% for my_page in sorted_pages %}
  {%- if my_page.menu_index and my_page.parent and my_page.parent == "behoeften" -%}{{ "" }}
## [{{ my_page.title }}]({{ my_page.url | prepend: site.baseurl }})
  {%- endif -%}
{% endfor %}

