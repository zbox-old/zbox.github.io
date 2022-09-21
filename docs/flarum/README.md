# Flarum

{% assign dir1 = page.dir | remove: "/" %}
{% assign dir2 = dir1 | append: "-" %}

{% assign group = site.github.public_repositories | where_exp: "i", "i.name contains dir2" %}
{% for i in group %}
  {% assign name = i.name | remove: dir2 %}
  <span class="block">[{{ name }}]({{ i.html_url }})</span>
  <span class="block"><small>{{ i.description }}</small></span>
  <span class="block">[README]({{ name }})</span>
{% endfor %}
