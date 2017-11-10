---
layout: default
published: true
---
# Welkom bij het slimme peuterproject!

Op deze website vind je informatie over peuters met een ontwikkelingsvoorsprong en vind je een stappenplan en ideeën voor het aanbieden van uitdagende activiteiten. 

<img src="/images/main-page.png" class="centered"/>

Het slimme peuterproject is ontworpen voor pedagogisch medewerkers die meer willen leren over peuters met een ontwikkelingsvoorsprong en op zoek zijn naar leuke uitdagende activiteiten! De website is een onderdeel van een cursus over slimme peuters. 

Via het menu of via de linkjes hieronder kun je snel naar alle informatie van het slimme peuterproject:

 {% assign sorted_pages = site.pages | sort:"menu_index" %}
{% for my_page in sorted_pages %}
  {% if my_page.menu_index and my_page.parent == "index" %}
## [{{ my_page.title }}]({{ my_page.url | prepend: site.baseurl }})
  {% endif %}
{% endfor %}
